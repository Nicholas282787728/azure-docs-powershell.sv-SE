---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: b3790105f2404cc7bf50ef1200ce0978e8f0b15d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582452"
---
# <span data-ttu-id="40221-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="40221-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="40221-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="40221-102">SYNOPSIS</span></span>
<span data-ttu-id="40221-103">Ställer in en policy för virtuella datorer per användare i ett labb i DevTest-labb.</span><span class="sxs-lookup"><span data-stu-id="40221-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40221-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="40221-104">SYNTAX</span></span>

### <span data-ttu-id="40221-105">Aktivera (standard)</span><span class="sxs-lookup"><span data-stu-id="40221-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40221-106">Aktiverar</span><span class="sxs-lookup"><span data-stu-id="40221-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40221-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="40221-107">DESCRIPTION</span></span>
<span data-ttu-id="40221-108">Cmdleten **set-AzureRmDtlVMsPerUserPolicy** anger de virtuella datorerna per användar princip för ett labb som anger det högsta antalet virtuella datorer som tillåts per användare.</span><span class="sxs-lookup"><span data-stu-id="40221-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="40221-109">Cmdleten använder den angivna resurs gruppen och namnet på laboratoriet för att ange principen.</span><span class="sxs-lookup"><span data-stu-id="40221-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="40221-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="40221-110">EXAMPLES</span></span>

## <span data-ttu-id="40221-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="40221-111">PARAMETERS</span></span>

### <span data-ttu-id="40221-112">-Inaktivera</span><span class="sxs-lookup"><span data-stu-id="40221-112">-Disable</span></span>
<span data-ttu-id="40221-113">Anger att denna cmdlet inaktiverar policyn för laboratoriet.</span><span class="sxs-lookup"><span data-stu-id="40221-113">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="40221-114">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="40221-114">-Enable</span></span>
<span data-ttu-id="40221-115">Anger att denna cmdlet aktiverar policyn för labbet.</span><span class="sxs-lookup"><span data-stu-id="40221-115">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="40221-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="40221-116">-LabName</span></span>
<span data-ttu-id="40221-117">Anger namnet på den Lab för vilken denna cmdlet ställer in principen för virtuella datorer per användare.</span><span class="sxs-lookup"><span data-stu-id="40221-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="40221-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="40221-118">-MaxVMs</span></span>
<span data-ttu-id="40221-119">Anger maximalt antal virtuella datorer som kan skapas i laboratorium.</span><span class="sxs-lookup"><span data-stu-id="40221-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="40221-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40221-120">-ResourceGroupName</span></span>
<span data-ttu-id="40221-121">Anger namnet på den resurs grupp som laboratoriet hör till.</span><span class="sxs-lookup"><span data-stu-id="40221-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="40221-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="40221-122">-Confirm</span></span>
<span data-ttu-id="40221-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="40221-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40221-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40221-124">-WhatIf</span></span>
<span data-ttu-id="40221-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="40221-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40221-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="40221-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40221-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40221-127">-DefaultProfile</span></span>
<span data-ttu-id="40221-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="40221-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40221-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40221-129">CommonParameters</span></span>
<span data-ttu-id="40221-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40221-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40221-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40221-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40221-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="40221-132">INPUTS</span></span>

## <span data-ttu-id="40221-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="40221-133">OUTPUTS</span></span>

### <span data-ttu-id="40221-134">Microsoft. Azure. commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="40221-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="40221-135">Denna cmdlet returnerar den princip som anger maximalt antal virtuella datorer som kan skapas av en användare i labbet.</span><span class="sxs-lookup"><span data-stu-id="40221-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="40221-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="40221-136">NOTES</span></span>

## <span data-ttu-id="40221-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="40221-137">RELATED LINKS</span></span>

[<span data-ttu-id="40221-138">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="40221-138">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


