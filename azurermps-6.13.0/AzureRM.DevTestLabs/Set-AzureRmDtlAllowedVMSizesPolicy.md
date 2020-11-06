---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 5d5ca3f06ec76f45a8bb33aa5d4b810283ffce97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576293"
---
# <span data-ttu-id="8bbe4-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="8bbe4-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="8bbe4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8bbe4-102">SYNOPSIS</span></span>
<span data-ttu-id="8bbe4-103">Ställer in en policy för tillåten virtuell dator storlek för en laboratorie i DevTest-labb.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bbe4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8bbe4-104">SYNTAX</span></span>

### <span data-ttu-id="8bbe4-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="8bbe4-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bbe4-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="8bbe4-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8bbe4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8bbe4-107">DESCRIPTION</span></span>
<span data-ttu-id="8bbe4-108">Cmdleten **set-AzureRmDtlAllowedVMSizesPolicy** anger den tillåtna principen för den virtuella dator storleken, som anger en lista över storlekar för virtuell dator som är tillåtna i en labb miljö.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="8bbe4-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="8bbe4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8bbe4-110">EXAMPLES</span></span>

## <span data-ttu-id="8bbe4-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8bbe4-111">PARAMETERS</span></span>

### <span data-ttu-id="8bbe4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bbe4-112">-DefaultProfile</span></span>
<span data-ttu-id="8bbe4-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8bbe4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bbe4-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="8bbe4-114">-Disable</span></span>
<span data-ttu-id="8bbe4-115">Anger att denna cmdlet inaktiverar principen.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bbe4-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="8bbe4-116">-Enable</span></span>
<span data-ttu-id="8bbe4-117">Anger att denna cmdlet aktiverar policyn.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bbe4-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="8bbe4-118">-LabName</span></span>
<span data-ttu-id="8bbe4-119">Anger namnet på den Lab för vilken denna cmdlet ställer in princip för virtuell dator storlek.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bbe4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bbe4-120">-ResourceGroupName</span></span>
<span data-ttu-id="8bbe4-121">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bbe4-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="8bbe4-122">-VmSizes</span></span>
<span data-ttu-id="8bbe4-123">Anger, som en sträng mat ris lista, som är tillåtna i Lab.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bbe4-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8bbe4-124">-Confirm</span></span>
<span data-ttu-id="8bbe4-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bbe4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bbe4-126">-WhatIf</span></span>
<span data-ttu-id="8bbe4-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bbe4-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bbe4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bbe4-129">CommonParameters</span></span>
<span data-ttu-id="8bbe4-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bbe4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bbe4-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bbe4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bbe4-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8bbe4-132">INPUTS</span></span>

### <span data-ttu-id="8bbe4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8bbe4-133">System.String</span></span>

## <span data-ttu-id="8bbe4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8bbe4-134">OUTPUTS</span></span>

### <span data-ttu-id="8bbe4-135">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8bbe4-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="8bbe4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8bbe4-136">NOTES</span></span>

## <span data-ttu-id="8bbe4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8bbe4-137">RELATED LINKS</span></span>

[<span data-ttu-id="8bbe4-138">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="8bbe4-138">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)


