# Xcode Code Snippets
      
### Installation

```
cd ~/Library/Developer/Xcode/UserData/CodeSnippets/
git init
git remote add burtlo git@github.com:burtlo/xcode-snippets.git
git pull burtlo master
```

###Expecta

#### `subwithpartial - `Subject + Partial Mock Subject

```objc
__block <#class#> *subject;
__block id partialSubject;

beforeEach(^{
    subject = [[<#class#> alloc] init];
    partialSubject = [OCMockObject partialMockForObject:subject];
    
    });

```
#### `stubandreturn - `Stub and Return

```objc
[[[<#instance#> stub] andReturn:<#data#>] <#method#>:[OCMArg any]];
```
#### `stub - `Stub for Void

```objc
[[<#instance#> stub] <#method#>];
```
#### `expectwithblock - `Expect With Block

```objc
[[<#subject#> expect] <#method#>:[OCMArg checkWithBlock:^BOOL(id value) {
    <#code#>
                return NO;
            }]];

```

###

#### `block-var - `Block Variable

```objc
__block <#class#> <#name#>;
```

###Cedar

#### `descit - `Describe + It

```objc
describe(@"<#subject#>", ^{
    it(@"should <#behavior#>", ^{
        expect(YES).toBeFalsy(); 
    });
});

```
#### `itshould - `It

```objc
it(@"should <#behavior#>", ^{
    expect(YES).toBeTruthy();
});

```
#### `after - `After Each

```objc
afterEach(^{
    <#code#> 
});

```
#### `before - `Before Each

```objc
beforeEach(^{
    <#code#>
});

```

###OCMock

#### `mockforprot - `Mock for Protocol

```objc
<#subject#> = [OCMockObject mockForProtocol:@protocol(<#protocol#>)];
```
#### `mockforclass - `Mock for Class

```objc
<#subject#> = [OCMockObject mockForClass:[<#class#> class]];
```
#### `expectvoid - `Expect for Void

```objc
[[[<#instance#> expect] <#method#>];
```
#### `expectandreturn - `Expect and Return

```objc
[[[<#instance#> expect] andReturn:<#data#>] <#method#>:[OCMArg any]];
```
