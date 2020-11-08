---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: a18222c40dc5c56bd2d67afb8d0df35b7aedc532
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090466"
---
# <span data-ttu-id="dc80b-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="dc80b-101">Get-AzAttestation</span></span>

## <span data-ttu-id="dc80b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dc80b-102">SYNOPSIS</span></span>
<span data-ttu-id="dc80b-103">Får ett intyg.</span><span class="sxs-lookup"><span data-stu-id="dc80b-103">Gets an attestation.</span></span>

## <span data-ttu-id="dc80b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dc80b-104">SYNTAX</span></span>

### <span data-ttu-id="dc80b-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dc80b-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc80b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc80b-106">ResourceIdParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc80b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dc80b-107">DESCRIPTION</span></span>
<span data-ttu-id="dc80b-108">Get-AzAttestation cmdlet får information om attesteringen i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="dc80b-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="dc80b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dc80b-109">EXAMPLES</span></span>

### <span data-ttu-id="dc80b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dc80b-110">Example 1</span></span>
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

<span data-ttu-id="dc80b-111">Hämta *pshtest* i resurs gruppen *PSH-test-RG*.</span><span class="sxs-lookup"><span data-stu-id="dc80b-111">Get Attestation Provider *pshtest* in Resource Group *psh-test-rg*.</span></span>

## <span data-ttu-id="dc80b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dc80b-112">PARAMETERS</span></span>

### <span data-ttu-id="dc80b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc80b-113">-DefaultProfile</span></span>
<span data-ttu-id="dc80b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dc80b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc80b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="dc80b-115">-Name</span></span>
<span data-ttu-id="dc80b-116">Namn på attestering.</span><span class="sxs-lookup"><span data-stu-id="dc80b-116">Attestation Name.</span></span>

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

### <span data-ttu-id="dc80b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc80b-117">-ResourceGroupName</span></span>
<span data-ttu-id="dc80b-118">Anger namnet på den resurs grupp som är kopplad till intyget.</span><span class="sxs-lookup"><span data-stu-id="dc80b-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

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

### <span data-ttu-id="dc80b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc80b-119">-ResourceId</span></span>
<span data-ttu-id="dc80b-120">Anger namnet på den ResourceID som är kopplad till den attestering som tillfrågas</span><span class="sxs-lookup"><span data-stu-id="dc80b-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

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

### <span data-ttu-id="dc80b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc80b-121">CommonParameters</span></span>
<span data-ttu-id="dc80b-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc80b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc80b-123">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc80b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc80b-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dc80b-124">INPUTS</span></span>

### <span data-ttu-id="dc80b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dc80b-125">System.String</span></span>

## <span data-ttu-id="dc80b-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dc80b-126">OUTPUTS</span></span>

### <span data-ttu-id="dc80b-127">Microsoft. Azure. commands. attestering. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="dc80b-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="dc80b-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dc80b-128">NOTES</span></span>

## <span data-ttu-id="dc80b-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dc80b-129">RELATED LINKS</span></span>
