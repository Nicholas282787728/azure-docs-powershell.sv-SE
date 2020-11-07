---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3bfd8aad0c88f6a2cd6dfb27124f92605b8a17b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757092"
---
# <span data-ttu-id="22cba-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="22cba-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="22cba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22cba-102">SYNOPSIS</span></span>
<span data-ttu-id="22cba-103">Ställer in de virtuella datorerna per labb policy för en laboratorie i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="22cba-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22cba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22cba-104">SYNTAX</span></span>

### <span data-ttu-id="22cba-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="22cba-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22cba-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="22cba-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22cba-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22cba-107">DESCRIPTION</span></span>
<span data-ttu-id="22cba-108">Cmdleten **set-AzureRmDtlVMsPerLabPolicy** anger de virtuella datorerna per Lab-princip för en labb lista som anger totalt antal virtuella datorer som är tillåtna i ett labb.</span><span class="sxs-lookup"><span data-stu-id="22cba-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="22cba-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="22cba-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="22cba-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22cba-110">EXAMPLES</span></span>

## <span data-ttu-id="22cba-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22cba-111">PARAMETERS</span></span>

### <span data-ttu-id="22cba-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cba-112">-DefaultProfile</span></span>
<span data-ttu-id="22cba-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="22cba-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22cba-114">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="22cba-114">-Disable</span></span>
<span data-ttu-id="22cba-115">Anger att denna cmdlet inaktiverar policyn för labbet.</span><span class="sxs-lookup"><span data-stu-id="22cba-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="22cba-116">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="22cba-116">-Enable</span></span>
<span data-ttu-id="22cba-117">Anger att denna cmdlet aktiverar policyn för labbet.</span><span class="sxs-lookup"><span data-stu-id="22cba-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="22cba-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="22cba-118">-LabName</span></span>
<span data-ttu-id="22cba-119">Anger namnet på den laboratorie som den här cmdleten ställer in de virtuella datorerna per Lab-princip för.</span><span class="sxs-lookup"><span data-stu-id="22cba-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="22cba-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="22cba-120">-MaxVMs</span></span>
<span data-ttu-id="22cba-121">Anger maximalt antal virtuella datorer som kan skapas i laboratorium.</span><span class="sxs-lookup"><span data-stu-id="22cba-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="22cba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cba-122">-ResourceGroupName</span></span>
<span data-ttu-id="22cba-123">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="22cba-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="22cba-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="22cba-124">-Confirm</span></span>
<span data-ttu-id="22cba-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="22cba-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22cba-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22cba-126">-WhatIf</span></span>
<span data-ttu-id="22cba-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="22cba-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22cba-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="22cba-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22cba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cba-129">CommonParameters</span></span>
<span data-ttu-id="22cba-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cba-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22cba-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cba-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22cba-132">INPUTS</span></span>

### <span data-ttu-id="22cba-133">System. String</span><span class="sxs-lookup"><span data-stu-id="22cba-133">System.String</span></span>

## <span data-ttu-id="22cba-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22cba-134">OUTPUTS</span></span>

### <span data-ttu-id="22cba-135">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="22cba-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="22cba-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22cba-136">NOTES</span></span>

## <span data-ttu-id="22cba-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22cba-137">RELATED LINKS</span></span>

[<span data-ttu-id="22cba-138">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="22cba-138">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)

