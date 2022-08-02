# [NOTES](../README.md) - [Golang](../golang.md) - Sintaxis


- [Generics](genericse)

Take me to [pookie](#pookie)

## Generics


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



<a name="pookie">1</a>