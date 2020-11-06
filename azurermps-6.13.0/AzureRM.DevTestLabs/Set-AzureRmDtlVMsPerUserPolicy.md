---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 10d903be6082aea7fd4b703a7637ce5405fb39e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577046"
---
# <span data-ttu-id="8fd77-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="8fd77-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="8fd77-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8fd77-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd77-103">Ställer in en policy för virtuella datorer per användare i ett labb i DevTest-labb.</span><span class="sxs-lookup"><span data-stu-id="8fd77-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fd77-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8fd77-104">SYNTAX</span></span>

### <span data-ttu-id="8fd77-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="8fd77-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fd77-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="8fd77-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fd77-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8fd77-107">DESCRIPTION</span></span>
<span data-ttu-id="8fd77-108">Cmdleten **set-AzureRmDtlVMsPerUserPolicy** anger de virtuella datorerna per användar princip för ett labb som anger det högsta antalet virtuella datorer som tillåts per användare.</span><span class="sxs-lookup"><span data-stu-id="8fd77-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="8fd77-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="8fd77-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="8fd77-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8fd77-110">EXAMPLES</span></span>

## <span data-ttu-id="8fd77-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8fd77-111">PARAMETERS</span></span>

### <span data-ttu-id="8fd77-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd77-112">-DefaultProfile</span></span>
<span data-ttu-id="8fd77-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8fd77-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8fd77-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="8fd77-114">-Disable</span></span>
<span data-ttu-id="8fd77-115">Anger att denna cmdlet inaktiverar policyn för laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="8fd77-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="8fd77-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="8fd77-116">-Enable</span></span>
<span data-ttu-id="8fd77-117">Anger att denna cmdlet aktiverar policyn för labbet.</span><span class="sxs-lookup"><span data-stu-id="8fd77-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="8fd77-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="8fd77-118">-LabName</span></span>
<span data-ttu-id="8fd77-119">Anger namnet på den Lab för vilken denna cmdlet ställer in principen för virtuella datorer per användare.</span><span class="sxs-lookup"><span data-stu-id="8fd77-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="8fd77-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="8fd77-120">-MaxVMs</span></span>
<span data-ttu-id="8fd77-121">Anger maximalt antal virtuella datorer som kan skapas i laboratorium.</span><span class="sxs-lookup"><span data-stu-id="8fd77-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="8fd77-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fd77-122">-ResourceGroupName</span></span>
<span data-ttu-id="8fd77-123">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="8fd77-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="8fd77-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8fd77-124">-Confirm</span></span>
<span data-ttu-id="8fd77-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8fd77-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fd77-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fd77-126">-WhatIf</span></span>
<span data-ttu-id="8fd77-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8fd77-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8fd77-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8fd77-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fd77-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd77-129">CommonParameters</span></span>
<span data-ttu-id="8fd77-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fd77-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd77-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fd77-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd77-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8fd77-132">INPUTS</span></span>

### <span data-ttu-id="8fd77-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8fd77-133">System.String</span></span>

## <span data-ttu-id="8fd77-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8fd77-134">OUTPUTS</span></span>

### <span data-ttu-id="8fd77-135">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8fd77-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="8fd77-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8fd77-136">NOTES</span></span>

## <span data-ttu-id="8fd77-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8fd77-137">RELATED LINKS</span></span>

[<span data-ttu-id="8fd77-138">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="8fd77-138">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


