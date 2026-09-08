<details>
<summary>Disclaimer</summary>
This repo primarily exists for personal use, and so projects I'm working on that have multiple programmers can share these utility/helper classes. Again, please note that these tools are built for my own projects; <b><ins>this means that they could change in functionality at any time</ins></b>. If you plan on using them long term, I strongly suggest sticking to one version/installing a packing and sticking to it, or paying very close attention to each update/commit. Feel free to use these in your own projects or base your own code off of mine, no credit needed; just don't claim it as your own.
</details>

# GameServices
A simple system that sort of acts as a replacement/substitute for static Instances.
```cs
void OnEnable() => GameServices.Register(this);
void OnDisable() => GameServices.Deregister(this);

void GetExamples()
{
    var service = GameServices.Get<SomeService>();
    bool hasOtherService = GameServices.TryGet(out SomeOtherService otherService);
    bool containsAnotherService = GameServices.Contains<AnotherService>();
}
async void GetAsyncExample()
{
    var service = await GetAsync<SomeService>();
}
```
