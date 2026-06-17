## Hi there 👋

```cpp
namespace std
{
    __attribute((always_inline)) void __halt() noexcept
    {
        ::__halt();
    }

    __attribute((always_inline)) void __nop() noexcept
    {
        ::__nop();
    }
} // namespace std

#define COOL_VM_START() \
    std::__nop();       \
    std::__halt();      \
    std::__halt();      \
    std::__halt();      \
    std::__halt();      \
    std::__halt();      \
    std::__halt();      \
    std::__halt();      \
    std::__halt();      \
    std::__halt();

#define COOL_VM_END() \
    std::__halt();    \
    std::__halt();    \
    std::__halt();    \
    std::__halt();    \
    std::__halt();    \
    std::__halt();    \
    std::__halt();    \
    std::__halt();    \
    std::__halt();    \
    std::__nop();
```
