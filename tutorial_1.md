### @flyoutOnly true

```package
pxt-sparkbit=github:kidspark/pxt-sparkbit
```

# Introduction to MakeCode

## Step 1

Place the ``||sparkbitO:rotate motor module||`` block in the ``||basic:forever||`` block.

```blocks
basic.forever(function () {
    sparkbitO.rotateMotorDuration(sparkbitO.__outputNumber(1), 100, Directions.Clockwise)
})
```

## Step 2

Press ``|Download|`` when finished and observe mechanism.

## Step 3

Change the direction and speed. Press ``|Download|`` when finished and observe mechanism.

<script src="https://makecode.com/gh-pages-embed.js"></script><script>makeCodeRender("{{ site.makecode.home_url }}", "{{ site.github.owner_name }}/{{ site.github.repository_name }}");</script>