# Snapshot report for `test/no-useless-fallback-in-spread.mjs`

The actual snapshot is saved in `no-useless-fallback-in-spread.mjs.snap`.

Generated by [AVA](https://avajs.dev).

## Invalid #1
      1 | const object = {...(foo || {})}

> Output

    `␊
      1 | const object = {...foo}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(foo || {})}␊
        |                            ^^ The empty object is useless.␊
    `

## Invalid #2
      1 | const object = {...(foo ?? {})}

> Output

    `␊
      1 | const object = {...foo}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(foo ?? {})}␊
        |                            ^^ The empty object is useless.␊
    `

## Invalid #3
      1 | const object = {...(foo ?? (( {} )))}

> Output

    `␊
      1 | const object = {...foo}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(foo ?? (( {} )))}␊
        |                               ^^ The empty object is useless.␊
    `

## Invalid #4
      1 | const object = {...((( foo )) ?? (( {} )))}

> Output

    `␊
      1 | const object = {...(( foo ))}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...((( foo )) ?? (( {} )))}␊
        |                                     ^^ The empty object is useless.␊
    `

## Invalid #5
      1 | const object = {...(( (( foo )) ?? (( {} )) ))}

> Output

    `␊
      1 | const object = {... (( foo )) }␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(( (( foo )) ?? (( {} )) ))}␊
        |                                       ^^ The empty object is useless.␊
    `

## Invalid #6
      1 | async ()=> ({...((await foo) || {})})

> Output

    `␊
      1 | async ()=> ({...(await foo)})␊
    `

> Error 1/1

    `␊
    > 1 | async ()=> ({...((await foo) || {})})␊
        |                                 ^^ The empty object is useless.␊
    `

## Invalid #7
      1 | const object = {...(0 || {})}

> Output

    `␊
      1 | const object = {...0}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(0 || {})}␊
        |                          ^^ The empty object is useless.␊
    `

## Invalid #8
      1 | const object = {...((-0) || {})}

> Output

    `␊
      1 | const object = {...(-0)}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...((-0) || {})}␊
        |                             ^^ The empty object is useless.␊
    `

## Invalid #9
      1 | const object = {...(.0 || {})}

> Output

    `␊
      1 | const object = {....0}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(.0 || {})}␊
        |                           ^^ The empty object is useless.␊
    `

## Invalid #10
      1 | const object = {...(0n || {})}

> Output

    `␊
      1 | const object = {...0n}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(0n || {})}␊
        |                           ^^ The empty object is useless.␊
    `

## Invalid #11
      1 | const object = {...(false || {})}

> Output

    `␊
      1 | const object = {...false}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(false || {})}␊
        |                              ^^ The empty object is useless.␊
    `

## Invalid #12
      1 | const object = {...(null || {})}

> Output

    `␊
      1 | const object = {...null}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(null || {})}␊
        |                             ^^ The empty object is useless.␊
    `

## Invalid #13
      1 | const object = {...(undefined || {})}

> Output

    `␊
      1 | const object = {...undefined}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(undefined || {})}␊
        |                                  ^^ The empty object is useless.␊
    `

## Invalid #14
      1 | const object = {...((a && b) || {})}

> Output

    `␊
      1 | const object = {...(a && b)}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...((a && b) || {})}␊
        |                                 ^^ The empty object is useless.␊
    `

## Invalid #15
      1 | const object = {...(NaN || {})}

> Output

    `␊
      1 | const object = {...NaN}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(NaN || {})}␊
        |                            ^^ The empty object is useless.␊
    `

## Invalid #16
      1 | const object = {...("" || {})}

> Output

    `␊
      1 | const object = {...""}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...("" || {})}␊
        |                           ^^ The empty object is useless.␊
    `

## Invalid #17
      1 | const object = {...([] || {})}

> Output

    `␊
      1 | const object = {...([])}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...([] || {})}␊
        |                           ^^ The empty object is useless.␊
    `

## Invalid #18
      1 | const object = {...({} || {})}

> Output

    `␊
      1 | const object = {...({})}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...({} || {})}␊
        |                           ^^ The empty object is useless.␊
    `

## Invalid #19
      1 | const object = {...(foo || {}),}

> Output

    `␊
      1 | const object = {...foo,}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(foo || {}),}␊
        |                            ^^ The empty object is useless.␊
    `

## Invalid #20
      1 | const object = {...((foo ?? {}) || {})}

> Output

    `␊
      1 | const object = {...foo}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...((foo ?? {}) || {})}␊
        |                                    ^^ The empty object is useless.␊
    `

## Invalid #21
      1 | const object = {...((foo && {}) || {})}

> Output

    `␊
      1 | const object = {...(foo && {})}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...((foo && {}) || {})}␊
        |                                    ^^ The empty object is useless.␊
    `

## Invalid #22
      1 | const object = {...(foo && {} || {})}

> Output

    `␊
      1 | const object = {...(foo && {})}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(foo && {} || {})}␊
        |                                  ^^ The empty object is useless.␊
    `

## Invalid #23
      1 | const object = {...({...(foo || {})})}

> Output

    `␊
      1 | const object = {...({...foo})}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...({...(foo || {})})}␊
        |                                 ^^ The empty object is useless.␊
    `

## Invalid #24
      1 | function foo(a = {...(bar || {})}){}

> Output

    `␊
      1 | function foo(a = {...bar}){}␊
    `

> Error 1/1

    `␊
    > 1 | function foo(a = {...(bar || {})}){}␊
        |                              ^^ The empty object is useless.␊
    `

## Invalid #25
      1 | const object = {...(document.all || {})}

> Output

    `␊
      1 | const object = {...document.all}␊
    `

> Error 1/1

    `␊
    > 1 | const object = {...(document.all || {})}␊
        |                                     ^^ The empty object is useless.␊
    `