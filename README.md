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
