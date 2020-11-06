---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: da4f9846f8fceaaecc6d4385374f6525d3243e3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574348"
---
# <span data-ttu-id="8f357-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8f357-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="8f357-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f357-102">SYNOPSIS</span></span>
<span data-ttu-id="8f357-103">Tar bort en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="8f357-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f357-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f357-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f357-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f357-105">DESCRIPTION</span></span>
<span data-ttu-id="8f357-106">Cmdleten **Remove-AzureRmContainerService** tar bort en behållar tjänst från ditt Azure-konto.</span><span class="sxs-lookup"><span data-stu-id="8f357-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="8f357-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f357-107">EXAMPLES</span></span>

### <span data-ttu-id="8f357-108">Exempel 1: ta bort en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="8f357-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="8f357-109">Det här kommandot tar bort behållar tjänsten med namnet CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="8f357-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="8f357-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f357-110">PARAMETERS</span></span>

### <span data-ttu-id="8f357-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8f357-111">-Force</span></span>
<span data-ttu-id="8f357-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="8f357-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f357-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f357-113">-Name</span></span>
<span data-ttu-id="8f357-114">Anger namnet på den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="8f357-114">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f357-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f357-115">-ResourceGroupName</span></span>
<span data-ttu-id="8f357-116">Anger resurs gruppen för den behållar tjänst som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="8f357-116">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8f357-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8f357-117">-Confirm</span></span>
<span data-ttu-id="8f357-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8f357-118">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f357-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f357-119">-WhatIf</span></span>
<span data-ttu-id="8f357-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8f357-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f357-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8f357-121">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f357-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f357-122">CommonParameters</span></span>
<span data-ttu-id="8f357-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f357-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f357-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f357-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f357-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f357-125">INPUTS</span></span>

### <span data-ttu-id="8f357-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="8f357-126">None</span></span>
<span data-ttu-id="8f357-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="8f357-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8f357-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f357-128">OUTPUTS</span></span>

## <span data-ttu-id="8f357-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f357-129">NOTES</span></span>

## <span data-ttu-id="8f357-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f357-130">RELATED LINKS</span></span>

[<span data-ttu-id="8f357-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8f357-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="8f357-132">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8f357-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="8f357-133">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8f357-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


