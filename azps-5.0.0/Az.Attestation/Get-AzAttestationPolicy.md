---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestationPolicy.md
ms.openlocfilehash: 64a74902d1a5b10ed36c635b58910246634e68b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270323"
---
# <span data-ttu-id="f59b8-101">Get-AzAttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="f59b8-101">Get-AzAttestationPolicy</span></span>

## <span data-ttu-id="f59b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f59b8-102">SYNOPSIS</span></span>
<span data-ttu-id="f59b8-103">Hämtar policyn från en innehavare i Azure-attestering.</span><span class="sxs-lookup"><span data-stu-id="f59b8-103">Gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f59b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f59b8-104">SYNTAX</span></span>

### <span data-ttu-id="f59b8-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f59b8-105">NameParameterSet</span></span>
```
Get-AzAttestationPolicy [-Name] <String> [-ResourceGroupName] <String> -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f59b8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f59b8-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestationPolicy [-ResourceId] <String> -Tee <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f59b8-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="f59b8-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestationPolicy [-Location] <String> [-DefaultProvider] -Tee <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f59b8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f59b8-108">DESCRIPTION</span></span>
<span data-ttu-id="f59b8-109">Get-AzAttestationPolicy cmdlet får principen från en innehavare i Azure-attestering.</span><span class="sxs-lookup"><span data-stu-id="f59b8-109">The Get-AzAttestationPolicy cmdlet gets the policy from a tenant in Azure Attestation.</span></span>

## <span data-ttu-id="f59b8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f59b8-110">EXAMPLES</span></span>

### <span data-ttu-id="f59b8-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f59b8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -Name pshtest -ResourceGroupName psh-test-rg -Tee SgxEnclave                                                                                                                                                                                                                    
Text       : version= 1.0;
             authorizationrules{
                 c:[type=="$is-debuggable"] => permit();
             };
             issuancerules{
                 c:[type=="$is-debuggable"] => issue(type="is-debuggable", value=c.value);
                 c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);
                 c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave", value=c.value);
                 c:[type=="$product-id"] => issue(type="product-id", value=c.value);
                 c:[type=="$svn"] => issue(type="svn", value=c.value);
                 c:[type=="$tee"] => issue(type="tee", value=c.value);
                 c:[type=="$tee-future"] => issue(type="tee-future", value=c.value);
             };

TextLength : 604
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3T3cwS1lYVjBhRzl5YVhwaGRHbHZibkoxYkdWemV3MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2FYTXRaR1ZpZFdkbllXSnNaU0pkSUQwLUlIQmxjbTFwZENncE93MEtmVHNOQ21semMzVmhibU5sY25Wc1pYTjdEUW9nSUNBZ1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2MyZDRMVzF5YzJsbmJtVnlJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGljMmQ0TFcxeWMybG5ibVZ5SWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVJ6WjNndGJYSmxibU5zWVhabElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWMyZDRMVzF5Wlc1amJHRjJaU0lzSUhaaGJIVmxQV011ZG1Gc2RXVXBPdzBLSUNBZ0lHTTZXM1I1Y0dVOVBTSWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHNOQ2lBZ0lDQmpPbHQwZVhCbFBUMGlKSE4yYmlKZElEMC1JR2x6YzNWbEtIUjVjR1U5SW5OMmJpSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE93MEtJQ0FnSUdNNlczUjVjR1U5UFNJa2RHVmxJbDBnUFQ0Z2FYTnpkV1VvZEhsd1pUMGlkR1ZsSWl3Z2RtRnNkV1U5WXk1MllXeDFaU2s3RFFvZ0lDQWdZenBiZEhsd1pUMDlJaVIwWldVdFpuVjBkWEpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpZEdWbExXWjFkSFZ5WlNJc0lIWmhiSFZsUFdNdWRtRnNkV1VwT3cwS2ZUc05DZyJ9.
JwtLength  : 1129
Algorithm  : none
```

<span data-ttu-id="f59b8-112">Hämtar policyn för *pshtest* för shirt ( *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="f59b8-112">Gets the policy for Attestation Provider *pshtest* for Tee type *SgxEnclave*.</span></span>

### <span data-ttu-id="f59b8-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f59b8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestationPolicy -DefaultProvider -Location "UK South" -Tee SgxEnclave
Text       : version= 1.0;authorizationrules{c:[type=="$is-debuggable"] => permit();};issuancerules{c:[type=="$is-debuggable"] => issue(type="is-debuggable",
             value=c.value);c:[type=="$sgx-mrsigner"] => issue(type="sgx-mrsigner", value=c.value);c:[type=="$sgx-mrenclave"] => issue(type="sgx-mrenclave",
             value=c.value);c:[type=="$product-id"] => issue(type="product-id", value=c.value);c:[type=="$svn"] => issue(type="svn", value=c.value);c:[type=="$tee"]
             => issue(type="tee", value=c.value);};
TextLength : 479
Jwt        : eyJhbGciOiJub25lIn0.eyJBdHRlc3RhdGlvblBvbGljeSI6ICJkbVZ5YzJsdmJqMGdNUzR3TzJGMWRHaHZjbWw2WVhScGIyNXlkV3hsYzN0ak9sdDBlWEJsUFQwaUpHbHpMV1JsWW5WbloyRmliR1Vp
             WFNBOVBpQndaWEp0YVhRb0tUdDlPMmx6YzNWaGJtTmxjblZzWlhON1l6cGJkSGx3WlQwOUlpUnBjeTFrWldKMVoyZGhZbXhsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYVhNdFpHVmlkV2RuWVdKc1pT
             SXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBTSWtjMmQ0TFcxeWMybG5ibVZ5SWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXljMmxuYm1WeUlpd2dkbUZzZFdVOVl5NTJZV3gx
             WlNrN1l6cGJkSGx3WlQwOUlpUnpaM2d0YlhKbGJtTnNZWFpsSWwwZ1BUNGdhWE56ZFdVb2RIbHdaVDBpYzJkNExXMXlaVzVqYkdGMlpTSXNJSFpoYkhWbFBXTXVkbUZzZFdVcE8yTTZXM1I1Y0dVOVBT
             SWtjSEp2WkhWamRDMXBaQ0pkSUQwLUlHbHpjM1ZsS0hSNWNHVTlJbkJ5YjJSMVkzUXRhV1FpTENCMllXeDFaVDFqTG5aaGJIVmxLVHRqT2x0MGVYQmxQVDBpSkhOMmJpSmRJRDAtSUdsemMzVmxLSFI1
             Y0dVOUluTjJiaUlzSUhaaGJIVmxQV011ZG1Gc2RXVXBPMk02VzNSNWNHVTlQU0lrZEdWbElsMGdQVDRnYVhOemRXVW9kSGx3WlQwaWRHVmxJaXdnZG1Gc2RXVTlZeTUyWVd4MVpTazdmVHMifQ.
JwtLength  : 907
Algorithm  : none
```

<span data-ttu-id="f59b8-114">Hämtar policyn för attestering standardprovider från plats *UK* för shirt (typ *SgxEnclave*.</span><span class="sxs-lookup"><span data-stu-id="f59b8-114">Gets the policy for Attestation Default Provider from Location *UK South* for Tee type *SgxEnclave*.</span></span>

## <span data-ttu-id="f59b8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f59b8-115">PARAMETERS</span></span>

### <span data-ttu-id="f59b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59b8-116">-DefaultProfile</span></span>
<span data-ttu-id="f59b8-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f59b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59b8-118">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="f59b8-118">-DefaultProvider</span></span>
<span data-ttu-id="f59b8-119">Anger det här begäran till en standardprovider för attestering.</span><span class="sxs-lookup"><span data-stu-id="f59b8-119">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59b8-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="f59b8-120">-Location</span></span>
<span data-ttu-id="f59b8-121">Anger platsen för standard leverantören för attestering.</span><span class="sxs-lookup"><span data-stu-id="f59b8-121">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59b8-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="f59b8-122">-Name</span></span>
<span data-ttu-id="f59b8-123">Anger ett namn på innehavaren.</span><span class="sxs-lookup"><span data-stu-id="f59b8-123">Specifies a name of the tenant.</span></span>
<span data-ttu-id="f59b8-124">Denna cmdlet hämtar policyn för attestering för den klient organisation som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f59b8-124">This cmdlet gets the attestation policy for the tenant that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f59b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="f59b8-126">Anger namnet på en attesterings leverantörs resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f59b8-126">Specifies the resource group name of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59b8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f59b8-127">-ResourceId</span></span>
<span data-ttu-id="f59b8-128">Anger ResourceID för en attesterings leverantör.</span><span class="sxs-lookup"><span data-stu-id="f59b8-128">Specifies the ResourceID of an attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59b8-129">-Shirt (</span><span class="sxs-lookup"><span data-stu-id="f59b8-129">-Tee</span></span>
<span data-ttu-id="f59b8-130">Anger en typ av körnings miljö.</span><span class="sxs-lookup"><span data-stu-id="f59b8-130">Specifies a type of Trusted Execution Environment.</span></span>
<span data-ttu-id="f59b8-131">Vi har stöd för fyra typer av miljöer: SgxEnclave, OpenEnclave, CyResComponent och VBSEnclave.</span><span class="sxs-lookup"><span data-stu-id="f59b8-131">We support four types of environment: SgxEnclave, OpenEnclave, CyResComponent and VBSEnclave.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59b8-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f59b8-132">-Confirm</span></span>
<span data-ttu-id="f59b8-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f59b8-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59b8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59b8-134">-WhatIf</span></span>
<span data-ttu-id="f59b8-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f59b8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f59b8-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f59b8-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59b8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59b8-137">CommonParameters</span></span>
<span data-ttu-id="f59b8-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59b8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59b8-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f59b8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59b8-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f59b8-140">INPUTS</span></span>

### <span data-ttu-id="f59b8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f59b8-141">System.String</span></span>

## <span data-ttu-id="f59b8-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f59b8-142">OUTPUTS</span></span>

### <span data-ttu-id="f59b8-143">Microsoft. Azure. commands. attestering. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f59b8-143">Microsoft.Azure.Commands.Attestation.Models.PSPolicy</span></span>

## <span data-ttu-id="f59b8-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f59b8-144">NOTES</span></span>

## <span data-ttu-id="f59b8-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f59b8-145">RELATED LINKS</span></span>
