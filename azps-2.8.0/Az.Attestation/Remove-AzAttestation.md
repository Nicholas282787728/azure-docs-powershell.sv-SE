---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745608"
---
# <span data-ttu-id="82627-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="82627-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="82627-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="82627-102">SYNOPSIS</span></span>
<span data-ttu-id="82627-103">Tar bort en attestering.</span><span class="sxs-lookup"><span data-stu-id="82627-103">Deletes an attestation.</span></span>

## <span data-ttu-id="82627-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="82627-104">SYNTAX</span></span>

### <span data-ttu-id="82627-105">ByAvailableAttestation (standard)</span><span class="sxs-lookup"><span data-stu-id="82627-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82627-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="82627-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82627-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="82627-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82627-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="82627-108">DESCRIPTION</span></span>
<span data-ttu-id="82627-109">Remove-AzAttestation-cmdleten tar bort angiven attestering.</span><span class="sxs-lookup"><span data-stu-id="82627-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="82627-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="82627-110">EXAMPLES</span></span>

### <span data-ttu-id="82627-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="82627-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="82627-112">Ta bort attestering "från aktuell prenumeration och resurs grupp" RG1 ".</span><span class="sxs-lookup"><span data-stu-id="82627-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="82627-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="82627-113">PARAMETERS</span></span>

### <span data-ttu-id="82627-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82627-114">-AsJob</span></span>
<span data-ttu-id="82627-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="82627-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82627-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82627-116">-DefaultProfile</span></span>
<span data-ttu-id="82627-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="82627-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82627-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82627-118">-InputObject</span></span>
<span data-ttu-id="82627-119">Attesterings objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="82627-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82627-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="82627-120">-Name</span></span>
<span data-ttu-id="82627-121">Anger namnet på den attestering som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="82627-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82627-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82627-122">-PassThru</span></span>
<span data-ttu-id="82627-123">Denna cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="82627-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="82627-124">Om denna växel anges returnerar den sant om den är klar.</span><span class="sxs-lookup"><span data-stu-id="82627-124">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82627-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82627-125">-ResourceGroupName</span></span>
<span data-ttu-id="82627-126">Anger namnet på resurs gruppen för Azure-attestering som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="82627-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82627-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82627-127">-ResourceId</span></span>
<span data-ttu-id="82627-128">Resurs-ID för attestering.</span><span class="sxs-lookup"><span data-stu-id="82627-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82627-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="82627-129">-Confirm</span></span>
<span data-ttu-id="82627-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="82627-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82627-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82627-131">-WhatIf</span></span>
<span data-ttu-id="82627-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="82627-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82627-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="82627-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82627-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82627-134">CommonParameters</span></span>
<span data-ttu-id="82627-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82627-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82627-136">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82627-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82627-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="82627-137">INPUTS</span></span>

### <span data-ttu-id="82627-138">System. String</span><span class="sxs-lookup"><span data-stu-id="82627-138">System.String</span></span>

### <span data-ttu-id="82627-139">Microsoft. Azure. commands. attestering. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="82627-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="82627-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="82627-140">OUTPUTS</span></span>

### <span data-ttu-id="82627-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82627-141">System.Boolean</span></span>

## <span data-ttu-id="82627-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="82627-142">NOTES</span></span>

## <span data-ttu-id="82627-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="82627-143">RELATED LINKS</span></span>
