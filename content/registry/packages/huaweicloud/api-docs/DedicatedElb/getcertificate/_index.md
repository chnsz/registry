
---
title: "getCertificate"
title_tag: "huaweicloud.DedicatedElb.getCertificate"
meta_desc: "Documentation for the huaweicloud.DedicatedElb.getCertificate function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Use this data source to get the certificate in HuaweiCloud Dedicated Load Balance (Dedicated ELB).


<div><pulumi-examples>

## Example Usage

<div><pulumi-chooser type="language" options="typescript,python,go,csharp,java,yaml"></pulumi-chooser></div>





<div>
<pulumi-choosable type="language" values="csharp">

```csharp
using System.Collections.Generic;
using Pulumi;
using Huaweicloud = Pulumi.Huaweicloud;

return await Deployment.RunAsync(() => 
{
    var config = new Config();
    var certificateName = config.RequireObject<dynamic>("certificateName");
    var test = Huaweicloud.DedicatedElb.GetCertificate.Invoke(new()
    {
        Name = certificateName,
    });

});
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="go">

```go
package main

import (
	"github.com/huaweicloud/pulumi-huaweicloud/sdk/go/huaweicloud/DedicatedElb"
	"github.com/pulumi/pulumi-huaweicloud/sdk/go/huaweicloud/DedicatedElb"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi/config"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		cfg := config.New(ctx, "")
		certificateName := cfg.RequireObject("certificateName")
		_, err := DedicatedElb.GetCertificate(ctx, &dedicatedelb.GetCertificateArgs{
			Name: certificateName,
		}, nil)
		if err != nil {
			return err
		}
		return nil
	})
}
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="java">

```java
package generated_program;

import com.pulumi.Context;
import com.pulumi.Pulumi;
import com.pulumi.core.Output;
import com.pulumi.huaweicloud.DedicatedElb.DedicatedElbFunctions;
import com.pulumi.huaweicloud.DedicatedElb.inputs.GetCertificateArgs;
import java.util.List;
import java.util.ArrayList;
import java.util.Map;
import java.io.File;
import java.nio.file.Files;
import java.nio.file.Paths;

public class App {
    public static void main(String[] args) {
        Pulumi.run(App::stack);
    }

    public static void stack(Context ctx) {
        final var config = ctx.config();
        final var certificateName = config.get("certificateName");
        final var test = DedicatedElbFunctions.getCertificate(GetCertificateArgs.builder()
            .name(certificateName)
            .build());

    }
}
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="python">

```python
import pulumi
import pulumi_huaweicloud as huaweicloud

config = pulumi.Config()
certificate_name = config.require_object("certificateName")
test = huaweicloud.DedicatedElb.get_certificate(name=certificate_name)
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="typescript">


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as huaweicloud from "@pulumi/huaweicloud";

const config = new pulumi.Config();
const certificateName = config.requireObject("certificateName");
const test = huaweicloud.DedicatedElb.getCertificate({
    name: certificateName,
});
```


</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="yaml">

```yaml
configuration:
  certificateName:
    type: dynamic
variables:
  test:
    Fn::Invoke:
      Function: huaweicloud:DedicatedElb:getCertificate
      Arguments:
        name: ${certificateName}
```


</pulumi-choosable>
</div>





</pulumi-examples></div>




## Using getCertificate {#using}

Two invocation forms are available. The direct form accepts plain
arguments and either blocks until the result value is available, or
returns a Promise-wrapped result. The output form accepts
Input-wrapped arguments and returns an Output-wrapped result.

<div>
<pulumi-chooser type="language" options="typescript,python,go,csharp,java,yaml"></pulumi-chooser>
</div>


<div>
<pulumi-choosable type="language" values="javascript,typescript">
<div class="highlight"
><pre class="chroma"><code class="language-typescript" data-lang="typescript"
><span class="k">function </span>getCertificate<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetCertificateArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetCertificateResult</a></span>></span
><span class="k">
function </span>getCertificateOutput<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetCertificateOutputArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Output&lt;<span class="nx"><a href="#result">GetCertificateResult</a></span>></span
></code></pre></div>
</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="python">
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"
><span class="k">def </span>get_certificate<span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">region</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> <span>GetCertificateResult</span
><span class="k">
def </span>get_certificate_output<span class="p">(</span><span class="nx">name</span><span class="p">:</span> <span class="nx">Optional[pulumi.Input[str]]</span> = None<span class="p">,</span>
                    <span class="nx">region</span><span class="p">:</span> <span class="nx">Optional[pulumi.Input[str]]</span> = None<span class="p">,</span>
                    <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> <span>Output[GetCertificateResult]</span
></code></pre></div>
</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="go">
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"
><span class="k">func </span>GetCertificate<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetCertificateArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetCertificateResult</a></span>, error)</span
><span class="k">
func </span>GetCertificateOutput<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetCertificateOutputArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) GetCertificateResultOutput</span
></code></pre></div>

&gt; Note: This function is named `GetCertificate` in the Go SDK.

</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="csharp">
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetCertificate </span><span class="p">
{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetCertificateResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetCertificateArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="k">
    public static </span>Output&lt;<span class="nx"><a href="#result">GetCertificateResult</a></span>> <span class="p">Invoke(</span><span class="nx">GetCertificateInvokeArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="java">
<div class="highlight"><pre class="chroma"><code class="language-java" data-lang="java"><span class="k">public static CompletableFuture&lt;<span class="nx"><a href="#result">GetCertificateResult</a></span>> </span>getCertificate<span class="p">(</span><span class="nx">GetCertificateArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx">InvokeOptions</span><span class="p"> </span><span class="nx">options<span class="p">)</span>
<span class="c">// Output-based functions aren't available in Java yet</span>
</code></pre></div>
</pulumi-choosable>
</div>


<div>
<pulumi-choosable type="language" values="yaml">
<div class="highlight"><pre class="chroma"><code class="language-yaml" data-lang="yaml"><span class="k">Fn::Invoke:</span>
<span class="k">&nbsp;&nbsp;Function:</span> huaweicloud:DedicatedElb/getCertificate:getCertificate
<span class="k">&nbsp;&nbsp;Arguments:</span>
<span class="c">&nbsp;&nbsp;&nbsp;&nbsp;# Arguments dictionary</span></code></pre></div>
</pulumi-choosable>
</div>



The following arguments are supported:


<div>
<pulumi-choosable type="language" values="csharp">
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The name of certificate. The value is case sensitive and does not supports fuzzy matching.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="region_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The region in which to obtain the Dedicated ELB certificate. If omitted, the
provider-level region will be used.</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="go">
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The name of certificate. The value is case sensitive and does not supports fuzzy matching.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="region_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The region in which to obtain the Dedicated ELB certificate. If omitted, the
provider-level region will be used.</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="java">
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_java" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>The name of certificate. The value is case sensitive and does not supports fuzzy matching.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="region_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_java" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>The region in which to obtain the Dedicated ELB certificate. If omitted, the
provider-level region will be used.</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="javascript,typescript">
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The name of certificate. The value is case sensitive and does not supports fuzzy matching.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="region_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The region in which to obtain the Dedicated ELB certificate. If omitted, the
provider-level region will be used.</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="python">
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>The name of certificate. The value is case sensitive and does not supports fuzzy matching.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="region_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>The region in which to obtain the Dedicated ELB certificate. If omitted, the
provider-level region will be used.</p>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="yaml">
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="name_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_yaml" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>The name of certificate. The value is case sensitive and does not supports fuzzy matching.</p>
</dd><dt class="property-optional"
            title="Optional">
        <span id="region_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_yaml" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>The region in which to obtain the Dedicated ELB certificate. If omitted, the
provider-level region will be used.</p>
</dd></dl>
</pulumi-choosable>
</div>




## getCertificate Result {#result}

The following output properties are available:



<div>
<pulumi-choosable type="language" values="csharp">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Human-readable description for the Certificate.</p>
</dd><dt class="property-"
            title="">
        <span id="domain_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#domain_csharp" style="color: inherit; text-decoration: inherit;">Domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The domain of the Certificate. This parameter is valid only when <code>type</code> is &quot;server&quot;.</p>
</dd><dt class="property-"
            title="">
        <span id="expiration_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#expiration_csharp" style="color: inherit; text-decoration: inherit;">Expiration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Indicates the time when the certificate expires.</p>
</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The provider-assigned unique ID for this managed resource.</p>
</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="region_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_csharp" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the certificate type. The value can be one of the following:</p>
<ul>
<li><code>server</code>: indicates the server certificate.</li>
<li><code>client</code>: indicates the CA certificate.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="go">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Human-readable description for the Certificate.</p>
</dd><dt class="property-"
            title="">
        <span id="domain_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#domain_go" style="color: inherit; text-decoration: inherit;">Domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The domain of the Certificate. This parameter is valid only when <code>type</code> is &quot;server&quot;.</p>
</dd><dt class="property-"
            title="">
        <span id="expiration_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#expiration_go" style="color: inherit; text-decoration: inherit;">Expiration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Indicates the time when the certificate expires.</p>
</dd><dt class="property-"
            title="">
        <span id="id_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The provider-assigned unique ID for this managed resource.</p>
</dd><dt class="property-"
            title="">
        <span id="name_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="region_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_go" style="color: inherit; text-decoration: inherit;">Region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="type_go">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the certificate type. The value can be one of the following:</p>
<ul>
<li><code>server</code>: indicates the server certificate.</li>
<li><code>client</code>: indicates the CA certificate.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="java">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_java" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Human-readable description for the Certificate.</p>
</dd><dt class="property-"
            title="">
        <span id="domain_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#domain_java" style="color: inherit; text-decoration: inherit;">domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>The domain of the Certificate. This parameter is valid only when <code>type</code> is &quot;server&quot;.</p>
</dd><dt class="property-"
            title="">
        <span id="expiration_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#expiration_java" style="color: inherit; text-decoration: inherit;">expiration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Indicates the time when the certificate expires.</p>
</dd><dt class="property-"
            title="">
        <span id="id_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_java" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>The provider-assigned unique ID for this managed resource.</p>
</dd><dt class="property-"
            title="">
        <span id="name_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_java" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="region_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_java" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="type_java">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#type_java" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the certificate type. The value can be one of the following:</p>
<ul>
<li><code>server</code>: indicates the server certificate.</li>
<li><code>client</code>: indicates the CA certificate.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="javascript,typescript">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Human-readable description for the Certificate.</p>
</dd><dt class="property-"
            title="">
        <span id="domain_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#domain_nodejs" style="color: inherit; text-decoration: inherit;">domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The domain of the Certificate. This parameter is valid only when <code>type</code> is &quot;server&quot;.</p>
</dd><dt class="property-"
            title="">
        <span id="expiration_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#expiration_nodejs" style="color: inherit; text-decoration: inherit;">expiration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Indicates the time when the certificate expires.</p>
</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>The provider-assigned unique ID for this managed resource.</p>
</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="region_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_nodejs" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd><p>Specifies the certificate type. The value can be one of the following:</p>
<ul>
<li><code>server</code>: indicates the server certificate.</li>
<li><code>client</code>: indicates the CA certificate.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="python">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>Human-readable description for the Certificate.</p>
</dd><dt class="property-"
            title="">
        <span id="domain_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#domain_python" style="color: inherit; text-decoration: inherit;">domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>The domain of the Certificate. This parameter is valid only when <code>type</code> is &quot;server&quot;.</p>
</dd><dt class="property-"
            title="">
        <span id="expiration_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#expiration_python" style="color: inherit; text-decoration: inherit;">expiration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>Indicates the time when the certificate expires.</p>
</dd><dt class="property-"
            title="">
        <span id="id_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>The provider-assigned unique ID for this managed resource.</p>
</dd><dt class="property-"
            title="">
        <span id="name_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="region_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_python" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="type_python">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd><p>Specifies the certificate type. The value can be one of the following:</p>
<ul>
<li><code>server</code>: indicates the server certificate.</li>
<li><code>client</code>: indicates the CA certificate.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>

<div>
<pulumi-choosable type="language" values="yaml">
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="description_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#description_yaml" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Human-readable description for the Certificate.</p>
</dd><dt class="property-"
            title="">
        <span id="domain_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#domain_yaml" style="color: inherit; text-decoration: inherit;">domain</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>The domain of the Certificate. This parameter is valid only when <code>type</code> is &quot;server&quot;.</p>
</dd><dt class="property-"
            title="">
        <span id="expiration_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#expiration_yaml" style="color: inherit; text-decoration: inherit;">expiration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Indicates the time when the certificate expires.</p>
</dd><dt class="property-"
            title="">
        <span id="id_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#id_yaml" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>The provider-assigned unique ID for this managed resource.</p>
</dd><dt class="property-"
            title="">
        <span id="name_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#name_yaml" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="region_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#region_yaml" style="color: inherit; text-decoration: inherit;">region</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd></dd><dt class="property-"
            title="">
        <span id="type_yaml">
<a data-swiftype-name="resource-property" data-swiftype-type="text" href="#type_yaml" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">String</span>
    </dt>
    <dd><p>Specifies the certificate type. The value can be one of the following:</p>
<ul>
<li><code>server</code>: indicates the server certificate.</li>
<li><code>client</code>: indicates the CA certificate.</li>
</ul>
</dd></dl>
</pulumi-choosable>
</div>





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/huaweicloud/pulumi-huaweicloud">https://github.com/huaweicloud/pulumi-huaweicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd><p>This Pulumi package is based on the <a href="https://github.com/huaweicloud/terraform-provider-huaweicloud"><code>huaweicloud</code> Terraform Provider</a>.</p>
</dd>
</dl>
