# [NOTES](../README.md) - [Golang](../golang.md) - Sintaxis


- [Generics](#genericse)
- [Closures](#closures)
- [Interfaces](#interfaces)

## Interfaces
<a name="interfaces"></a>

        package main

        import "fmt"

        type animal soundMove

        type soundMove interface {
            volume()
        }

        type cat struct{}

        func (c *cat) volume() {
            fmt.Println("MEOW!")
        }

        func main() {
            var c animal = &cat{}

            c.volume()
        }


## Closures
<a name="closures"></a>

        package main

        import "fmt"

        func intSeq() func() int {
            i := 0
            return func() int {
                i++
                return i
            }
        }

        func main() {

            nextInt := intSeq()

            fmt.Println(nextInt())
            fmt.Println(nextInt())
            fmt.Println(nextInt())

            newInts := intSeq()
            fmt.Println(newInts())
        }

## Generics
<a name="genericse"></a>

        package main

        import "fmt"

        func main() {
            ss := []string{"a", "b"}
            nn := []int{1, 2}
            PrintSlise(ss)
            PrintSlise(nn)
        }

        func PrintSlise[T any](vv []T) {
            for _, v := range vv {
                fmt.Println(v)
            }
        }

        func Constain[T comparable](v T, vv []T) bool {
            for _, a := range vv {
                if a == v {
                    return true
                }
            }
            return false
        }

        func ConstainStr(v string, vv []string) bool {
            for _, a := range vv {
                if a == v {
                    return true
                }
            }
            return false
        }

        func ConstainInt(v int, vv []int) bool {
            for _, a := range vv {
                if a == v {
                    return true
                }
            }
            return false
        }



