---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: 650ac7c478f1c27ca3ba925c4d767f02c79fa781
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422875"
---
# <span data-ttu-id="a6af7-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="a6af7-101">Get-AzAttestation</span></span>

## <span data-ttu-id="a6af7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6af7-102">SYNOPSIS</span></span>
<span data-ttu-id="a6af7-103">Får ett intyg.</span><span class="sxs-lookup"><span data-stu-id="a6af7-103">Gets an attestation.</span></span>

## <span data-ttu-id="a6af7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6af7-104">SYNTAX</span></span>

### <span data-ttu-id="a6af7-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a6af7-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6af7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6af7-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6af7-107">DefaultProviderParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6af7-107">DefaultProviderParameterSet</span></span>
```
Get-AzAttestation [[-Location] <String>] [-DefaultProvider] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6af7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6af7-108">DESCRIPTION</span></span>
<span data-ttu-id="a6af7-109">Get-AzAttestation cmdlet får information om attesteringen i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="a6af7-109">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="a6af7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6af7-110">EXAMPLES</span></span>

### <span data-ttu-id="a6af7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a6af7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name pshtest -ResourceGroupName psh-test-rg                                                                                                                                                                                                                                                       
Id                : subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/psh-test-rg/providers/Microsoft.Attestation/attestationProviders/pshtest
Location          : East US
ResourceGroupName : psh-test-rg
Name              : pshtest
Status            : Ready
TrustModel        : AAD
AttestUri         : https://pshtest.us.attest.azure.net
Tags              : {Production, Example}
TagsTable         :
                    Name        Value
                    ==========  =====
                    Production  False
                    Example     True
```

<span data-ttu-id="a6af7-112">Hämta *pshtest* i resurs gruppen *PSH-test-RG*.</span><span class="sxs-lookup"><span data-stu-id="a6af7-112">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

### <span data-ttu-id="a6af7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a6af7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/sharedcus
Location          : Central US
ResourceGroupName :
Name              : sharedcus
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedcus.cus.attest.azure.net
Tags              :
TagsTable         :

Id                : /providers/Microsoft.Attestation/attestationProviders/shareduks
Location          : UK South
ResourceGroupName :
Name              : shareduks
Status            : Ready
TrustModel        : AAD
AttestUri         : https://shareduks.uks.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="a6af7-114">Skaffa alla tillgängliga standardprovidrar för attestering</span><span class="sxs-lookup"><span data-stu-id="a6af7-114">Get all available Attestation Default Providers</span></span>

### <span data-ttu-id="a6af7-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a6af7-115">Example 3</span></span>
```powershell
PS C:\> Get-AzAttestation -DefaultProvider -Location "East US 2"
Id                : /providers/Microsoft.Attestation/attestationProviders/sharedeus2
Location          : East US 2
ResourceGroupName :
Name              : sharedeus2
Status            : Ready
TrustModel        : AAD
AttestUri         : https://sharedeus2.eus2.attest.azure.net
Tags              :
TagsTable         :
```

<span data-ttu-id="a6af7-116">Hämta standardprovider för attestering från plats *östra USA 2*</span><span class="sxs-lookup"><span data-stu-id="a6af7-116">Get Attestation Default Provider from Location *East US 2*</span></span>

## <span data-ttu-id="a6af7-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6af7-117">PARAMETERS</span></span>

### <span data-ttu-id="a6af7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6af7-118">-DefaultProfile</span></span>
<span data-ttu-id="a6af7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a6af7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6af7-120">-DefaultProvider</span><span class="sxs-lookup"><span data-stu-id="a6af7-120">-DefaultProvider</span></span>
<span data-ttu-id="a6af7-121">Anger det här begäran till en standardprovider för attestering.</span><span class="sxs-lookup"><span data-stu-id="a6af7-121">Specifies this is the request to a default attestation provider.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6af7-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="a6af7-122">-Location</span></span>
<span data-ttu-id="a6af7-123">Anger platsen för standard leverantören för attestering.</span><span class="sxs-lookup"><span data-stu-id="a6af7-123">Specifies the Location of the default attestation provider.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultProviderParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6af7-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a6af7-124">-Name</span></span>
<span data-ttu-id="a6af7-125">Namn på attestering.</span><span class="sxs-lookup"><span data-stu-id="a6af7-125">Attestation Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6af7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6af7-126">-ResourceGroupName</span></span>
<span data-ttu-id="a6af7-127">Anger namnet på den resurs grupp som är kopplad till intyget.</span><span class="sxs-lookup"><span data-stu-id="a6af7-127">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6af7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6af7-128">-ResourceId</span></span>
<span data-ttu-id="a6af7-129">Anger namnet på den ResourceID som är kopplad till den attestering som tillfrågas</span><span class="sxs-lookup"><span data-stu-id="a6af7-129">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="a6af7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6af7-130">CommonParameters</span></span>
<span data-ttu-id="a6af7-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6af7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6af7-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6af7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6af7-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6af7-133">INPUTS</span></span>

### <span data-ttu-id="a6af7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a6af7-134">System.String</span></span>

## <span data-ttu-id="a6af7-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6af7-135">OUTPUTS</span></span>

### <span data-ttu-id="a6af7-136">Microsoft. Azure. commands. attestering. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="a6af7-136">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="a6af7-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6af7-137">NOTES</span></span>

## <span data-ttu-id="a6af7-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6af7-138">RELATED LINKS</span></span>
