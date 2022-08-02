# NOTES
<p align="left">
<img src="https://img.shields.io/badge/Golang-blue?style=for-the-badge" alt="">
</p>

Заметки по лекциям

- [Golang](golang/golang.md "Golang")
    - [Sintaxis](golang/sintaxis/sintaxis.md)
        - [Generics]()
    ---
    - [Gin]()
    - [Gorm]()

- [SQL]()
    - [Postgres]()

- [Docker]()

- [Test]()

- [В.мат.]()

- [Полезности]()

---

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





