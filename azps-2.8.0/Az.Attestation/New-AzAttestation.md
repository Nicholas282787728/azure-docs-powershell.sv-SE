---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/new-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/New-AzAttestation.md
ms.openlocfilehash: ce21b116ceb41bfdfb26008dd44c914f3198ab39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745609"
---
# <span data-ttu-id="380ef-101">New-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="380ef-101">New-AzAttestation</span></span>

## <span data-ttu-id="380ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="380ef-102">SYNOPSIS</span></span>
<span data-ttu-id="380ef-103">Skapar en attestering</span><span class="sxs-lookup"><span data-stu-id="380ef-103">Creates an attestation</span></span>

## <span data-ttu-id="380ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="380ef-104">SYNTAX</span></span>

```
New-AzAttestation -Name <String> -ResourceGroupName <String> [-AttestationPolicy <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="380ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="380ef-105">DESCRIPTION</span></span>
<span data-ttu-id="380ef-106">New-AzAttestation cmdlet skapar en attestering i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="380ef-106">The New-AzAttestation cmdlet creates an attestation in the specified resource group.</span></span>

## <span data-ttu-id="380ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="380ef-107">EXAMPLES</span></span>

### <span data-ttu-id="380ef-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="380ef-108">Example 1</span></span>
```powershell
PS C:\> New-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```

<span data-ttu-id="380ef-109">Skapa ett nytt intyg "i aktuell prenumeration, resurs grupp" RG1 "</span><span class="sxs-lookup"><span data-stu-id="380ef-109">Create a new Attestation "example" in current Subscription, Resource Group "rg1"</span></span>

## <span data-ttu-id="380ef-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="380ef-110">PARAMETERS</span></span>

### <span data-ttu-id="380ef-111">-AttestationPolicy</span><span class="sxs-lookup"><span data-stu-id="380ef-111">-AttestationPolicy</span></span>
<span data-ttu-id="380ef-112">Anger den policy för attestering som har överförts för att skapa attesteringen.</span><span class="sxs-lookup"><span data-stu-id="380ef-112">Specifies the attestation policy passed in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380ef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380ef-113">-DefaultProfile</span></span>
<span data-ttu-id="380ef-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="380ef-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="380ef-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="380ef-115">-Name</span></span>
<span data-ttu-id="380ef-116">Anger namnet på den instans som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="380ef-116">Specifies a name of the Instance to create.</span></span>
<span data-ttu-id="380ef-117">Namnet kan vara en kombination av bokstäver, siffror och bindestreck.</span><span class="sxs-lookup"><span data-stu-id="380ef-117">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="380ef-118">Namnet måste börja och sluta med en bokstav eller en siffra.</span><span class="sxs-lookup"><span data-stu-id="380ef-118">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="380ef-119">Namnet måste vara globalt unikt.</span><span class="sxs-lookup"><span data-stu-id="380ef-119">The name must be universally unique.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380ef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="380ef-120">-ResourceGroupName</span></span>
<span data-ttu-id="380ef-121">Anger namnet på en befintlig resurs grupp där attesteringen ska skapas.</span><span class="sxs-lookup"><span data-stu-id="380ef-121">Specifies the name of an existing resource group in which to create the attestation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380ef-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="380ef-122">-Confirm</span></span>
<span data-ttu-id="380ef-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="380ef-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ef-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="380ef-124">-WhatIf</span></span>
<span data-ttu-id="380ef-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="380ef-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="380ef-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="380ef-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="380ef-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380ef-127">CommonParameters</span></span>
<span data-ttu-id="380ef-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380ef-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380ef-129">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="380ef-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380ef-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="380ef-130">INPUTS</span></span>

### <span data-ttu-id="380ef-131">System. String</span><span class="sxs-lookup"><span data-stu-id="380ef-131">System.String</span></span>

## <span data-ttu-id="380ef-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="380ef-132">OUTPUTS</span></span>

### <span data-ttu-id="380ef-133">Microsoft. Azure. commands. attestering. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="380ef-133">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="380ef-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="380ef-134">NOTES</span></span>

## <span data-ttu-id="380ef-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="380ef-135">RELATED LINKS</span></span>
