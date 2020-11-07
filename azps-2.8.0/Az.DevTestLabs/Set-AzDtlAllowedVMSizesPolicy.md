---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 9d41e3c4c91a61a12ac18becb4b996bfbe52dbb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744332"
---
# <span data-ttu-id="b73bb-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="b73bb-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="b73bb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b73bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b73bb-103">Ställer in en policy för tillåten virtuell dator storlek för en laboratorie i DevTest-labb.</span><span class="sxs-lookup"><span data-stu-id="b73bb-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="b73bb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b73bb-104">SYNTAX</span></span>

### <span data-ttu-id="b73bb-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="b73bb-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b73bb-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="b73bb-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b73bb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b73bb-107">DESCRIPTION</span></span>
<span data-ttu-id="b73bb-108">Cmdleten **set-AzDtlAllowedVMSizesPolicy** anger den tillåtna principen för den virtuella dator storleken, som anger en lista över storlekar för virtuell dator som är tillåtna i en labb miljö.</span><span class="sxs-lookup"><span data-stu-id="b73bb-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="b73bb-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="b73bb-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="b73bb-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b73bb-110">EXAMPLES</span></span>

## <span data-ttu-id="b73bb-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b73bb-111">PARAMETERS</span></span>

### <span data-ttu-id="b73bb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73bb-112">-DefaultProfile</span></span>
<span data-ttu-id="b73bb-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="b73bb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b73bb-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="b73bb-114">-Disable</span></span>
<span data-ttu-id="b73bb-115">Anger att denna cmdlet inaktiverar principen.</span><span class="sxs-lookup"><span data-stu-id="b73bb-115">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="b73bb-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="b73bb-116">-Enable</span></span>
<span data-ttu-id="b73bb-117">Anger att denna cmdlet aktiverar policyn.</span><span class="sxs-lookup"><span data-stu-id="b73bb-117">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="b73bb-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="b73bb-118">-LabName</span></span>
<span data-ttu-id="b73bb-119">Anger namnet på den Lab för vilken denna cmdlet ställer in princip för virtuell dator storlek.</span><span class="sxs-lookup"><span data-stu-id="b73bb-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="b73bb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b73bb-120">-ResourceGroupName</span></span>
<span data-ttu-id="b73bb-121">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="b73bb-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="b73bb-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="b73bb-122">-VmSizes</span></span>
<span data-ttu-id="b73bb-123">Anger, som en sträng mat ris lista, som är tillåtna i Lab.</span><span class="sxs-lookup"><span data-stu-id="b73bb-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="b73bb-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b73bb-124">-Confirm</span></span>
<span data-ttu-id="b73bb-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b73bb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b73bb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b73bb-126">-WhatIf</span></span>
<span data-ttu-id="b73bb-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b73bb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b73bb-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b73bb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b73bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73bb-129">CommonParameters</span></span>
<span data-ttu-id="b73bb-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b73bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73bb-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b73bb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73bb-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b73bb-132">INPUTS</span></span>

### <span data-ttu-id="b73bb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b73bb-133">System.String</span></span>

## <span data-ttu-id="b73bb-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b73bb-134">OUTPUTS</span></span>

### <span data-ttu-id="b73bb-135">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b73bb-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="b73bb-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b73bb-136">NOTES</span></span>

## <span data-ttu-id="b73bb-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b73bb-137">RELATED LINKS</span></span>

[<span data-ttu-id="b73bb-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="b73bb-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


