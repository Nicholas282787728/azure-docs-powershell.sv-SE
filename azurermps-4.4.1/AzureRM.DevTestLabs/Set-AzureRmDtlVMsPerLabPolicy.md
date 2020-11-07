---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 95908e6b0976baf2ce9f3c117f54a6f1552e4957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756966"
---
# <span data-ttu-id="c46da-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="c46da-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="c46da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c46da-102">SYNOPSIS</span></span>
<span data-ttu-id="c46da-103">Ställer in de virtuella datorerna per labb policy för en laboratorie i DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="c46da-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c46da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c46da-104">SYNTAX</span></span>

### <span data-ttu-id="c46da-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="c46da-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c46da-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="c46da-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c46da-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c46da-107">DESCRIPTION</span></span>
<span data-ttu-id="c46da-108">Cmdleten **set-AzureRmDtlVMsPerLabPolicy** anger de virtuella datorerna per Lab-princip för en labb lista som anger totalt antal virtuella datorer som är tillåtna i ett labb.</span><span class="sxs-lookup"><span data-stu-id="c46da-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="c46da-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="c46da-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="c46da-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c46da-110">EXAMPLES</span></span>

## <span data-ttu-id="c46da-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c46da-111">PARAMETERS</span></span>

### <span data-ttu-id="c46da-112">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="c46da-112">-Disable</span></span>
<span data-ttu-id="c46da-113">Anger att denna cmdlet inaktiverar policyn för labbet.</span><span class="sxs-lookup"><span data-stu-id="c46da-113">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="c46da-114">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="c46da-114">-Enable</span></span>
<span data-ttu-id="c46da-115">Anger att denna cmdlet aktiverar policyn för labbet.</span><span class="sxs-lookup"><span data-stu-id="c46da-115">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="c46da-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="c46da-116">-LabName</span></span>
<span data-ttu-id="c46da-117">Anger namnet på den laboratorie som den här cmdleten ställer in de virtuella datorerna per Lab-princip för.</span><span class="sxs-lookup"><span data-stu-id="c46da-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="c46da-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="c46da-118">-MaxVMs</span></span>
<span data-ttu-id="c46da-119">Anger maximalt antal virtuella datorer som kan skapas i laboratorium.</span><span class="sxs-lookup"><span data-stu-id="c46da-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="c46da-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c46da-120">-ResourceGroupName</span></span>
<span data-ttu-id="c46da-121">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="c46da-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="c46da-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c46da-122">-Confirm</span></span>
<span data-ttu-id="c46da-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c46da-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c46da-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c46da-124">-WhatIf</span></span>
<span data-ttu-id="c46da-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c46da-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c46da-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c46da-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c46da-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c46da-127">-DefaultProfile</span></span>
<span data-ttu-id="c46da-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c46da-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c46da-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c46da-129">CommonParameters</span></span>
<span data-ttu-id="c46da-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c46da-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c46da-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c46da-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c46da-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c46da-132">INPUTS</span></span>

## <span data-ttu-id="c46da-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c46da-133">OUTPUTS</span></span>

### <span data-ttu-id="c46da-134">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="c46da-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="c46da-135">Denna cmdlet returnerar den princip som anger maximalt antal virtuella datorer som kan skapas i Lab.</span><span class="sxs-lookup"><span data-stu-id="c46da-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="c46da-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c46da-136">NOTES</span></span>

## <span data-ttu-id="c46da-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c46da-137">RELATED LINKS</span></span>

[<span data-ttu-id="c46da-138">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="c46da-138">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)


