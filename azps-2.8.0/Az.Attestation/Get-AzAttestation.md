---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745610"
---
# <span data-ttu-id="9acba-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="9acba-101">Get-AzAttestation</span></span>

## <span data-ttu-id="9acba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9acba-102">SYNOPSIS</span></span>
<span data-ttu-id="9acba-103">Får ett intyg.</span><span class="sxs-lookup"><span data-stu-id="9acba-103">Gets an attestation.</span></span>

## <span data-ttu-id="9acba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9acba-104">SYNTAX</span></span>

### <span data-ttu-id="9acba-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9acba-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9acba-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="9acba-106">ResourceGroupParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9acba-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9acba-107">DESCRIPTION</span></span>
<span data-ttu-id="9acba-108">Get-AzAttestation cmdlet får information om attesteringen i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="9acba-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="9acba-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9acba-109">EXAMPLES</span></span>

### <span data-ttu-id="9acba-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9acba-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
<span data-ttu-id="9acba-111">Skaffa attestering "i resurs gruppen" RG1 ".</span><span class="sxs-lookup"><span data-stu-id="9acba-111">Get Attestation "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="9acba-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9acba-112">PARAMETERS</span></span>

### <span data-ttu-id="9acba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9acba-113">-DefaultProfile</span></span>
<span data-ttu-id="9acba-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9acba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9acba-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="9acba-115">-Name</span></span>
<span data-ttu-id="9acba-116">Namn på attestering.</span><span class="sxs-lookup"><span data-stu-id="9acba-116">Attestation Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9acba-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9acba-117">-ResourceGroupName</span></span>
<span data-ttu-id="9acba-118">Anger namnet på den resurs grupp som är kopplad till intyget.</span><span class="sxs-lookup"><span data-stu-id="9acba-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9acba-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9acba-119">-ResourceId</span></span>
<span data-ttu-id="9acba-120">Anger namnet på den ResourceID som är kopplad till den attestering som tillfrågas</span><span class="sxs-lookup"><span data-stu-id="9acba-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9acba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9acba-121">CommonParameters</span></span>
<span data-ttu-id="9acba-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9acba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9acba-123">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9acba-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9acba-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9acba-124">INPUTS</span></span>

### <span data-ttu-id="9acba-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9acba-125">System.String</span></span>

## <span data-ttu-id="9acba-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9acba-126">OUTPUTS</span></span>

### <span data-ttu-id="9acba-127">Microsoft. Azure. commands. attestering. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="9acba-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="9acba-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9acba-128">NOTES</span></span>

## <span data-ttu-id="9acba-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9acba-129">RELATED LINKS</span></span>
