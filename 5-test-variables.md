```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# Test Variables

## step 1

with "let" 0

```blocks
let count = 0
```

## Step 2

without "let" 0

```blocks
count = 0
```

## Step 4

with "let" false

```blocks
let toggle = false
```

## Step 5

without "let" false

```blocks
toggle = false
```

## Step 6

blocks then image

```blocks
basic.forever(function () {
    basic.showNumber(0)
})
```

![set count](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/3-3-set-count.png)

## Step 7

image then blocks

![set count](https://raw.githubusercontent.com/KidSpark/tutorials/master/assets/3-3-set-count.png)

```blocks
basic.forever(function () {
    basic.showNumber(0)
})
```