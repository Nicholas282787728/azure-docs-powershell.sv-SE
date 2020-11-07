---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 33f60d8246f7235e4be816ad55b69c2ebafe9b0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754170"
---
# <span data-ttu-id="c0394-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="c0394-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="c0394-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0394-102">SYNOPSIS</span></span>
<span data-ttu-id="c0394-103">Ställer in en policy för virtuella datorer per användare i ett labb i DevTest-labb.</span><span class="sxs-lookup"><span data-stu-id="c0394-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="c0394-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0394-104">SYNTAX</span></span>

### <span data-ttu-id="c0394-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="c0394-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0394-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="c0394-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0394-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0394-107">DESCRIPTION</span></span>
<span data-ttu-id="c0394-108">Cmdleten **set-AzDtlVMsPerUserPolicy** anger de virtuella datorerna per användar princip för ett labb som anger det högsta antalet virtuella datorer som tillåts per användare.</span><span class="sxs-lookup"><span data-stu-id="c0394-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="c0394-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="c0394-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="c0394-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0394-110">EXAMPLES</span></span>

## <span data-ttu-id="c0394-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0394-111">PARAMETERS</span></span>

### <span data-ttu-id="c0394-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0394-112">-DefaultProfile</span></span>
<span data-ttu-id="c0394-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c0394-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0394-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="c0394-114">-Disable</span></span>
<span data-ttu-id="c0394-115">Anger att denna cmdlet inaktiverar policyn för laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="c0394-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="c0394-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="c0394-116">-Enable</span></span>
<span data-ttu-id="c0394-117">Anger att denna cmdlet aktiverar policyn för labbet.</span><span class="sxs-lookup"><span data-stu-id="c0394-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="c0394-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="c0394-118">-LabName</span></span>
<span data-ttu-id="c0394-119">Anger namnet på den Lab för vilken denna cmdlet ställer in principen för virtuella datorer per användare.</span><span class="sxs-lookup"><span data-stu-id="c0394-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="c0394-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="c0394-120">-MaxVMs</span></span>
<span data-ttu-id="c0394-121">Anger maximalt antal virtuella datorer som kan skapas i laboratorium.</span><span class="sxs-lookup"><span data-stu-id="c0394-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0394-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0394-122">-ResourceGroupName</span></span>
<span data-ttu-id="c0394-123">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="c0394-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="c0394-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0394-124">-Confirm</span></span>
<span data-ttu-id="c0394-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0394-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0394-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0394-126">-WhatIf</span></span>
<span data-ttu-id="c0394-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0394-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0394-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0394-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0394-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0394-129">CommonParameters</span></span>
<span data-ttu-id="c0394-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0394-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0394-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0394-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0394-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0394-132">INPUTS</span></span>

### <span data-ttu-id="c0394-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c0394-133">System.String</span></span>

## <span data-ttu-id="c0394-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0394-134">OUTPUTS</span></span>

### <span data-ttu-id="c0394-135">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c0394-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="c0394-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0394-136">NOTES</span></span>

## <span data-ttu-id="c0394-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0394-137">RELATED LINKS</span></span>

[<span data-ttu-id="c0394-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="c0394-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)

