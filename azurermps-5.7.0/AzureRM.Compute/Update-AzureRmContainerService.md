---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: 62acfacbafb50f85673b37e802b9d0b0eb4bf66a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573504"
---
# <span data-ttu-id="f216f-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f216f-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="f216f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f216f-102">SYNOPSIS</span></span>
<span data-ttu-id="f216f-103">Uppdaterar tillståndet för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="f216f-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f216f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f216f-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <ContainerService> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f216f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f216f-105">DESCRIPTION</span></span>
<span data-ttu-id="f216f-106">Cmdleten **Update-AzureRmContainerService** uppdaterar statusen för en behållar tjänst så att den matchar en lokal instans av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="f216f-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="f216f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f216f-107">EXAMPLES</span></span>

### <span data-ttu-id="f216f-108">Exempel 1: uppdatera en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="f216f-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="f216f-109">Med det här kommandot hämtas behållar tjänsten med namnet CSResourceGroup17 med hjälp av Get-AzureRmContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f216f-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="f216f-110">Kommandot skickar detta objekt till Remove-AzureRmContainerServiceAgentPoolProfile cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="f216f-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="f216f-111">**Remove-AzureRmContainerServiceAgentPoolProfile** tar bort profilen med namnet AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="f216f-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="f216f-112">Kommandot skickar resultatet till Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f216f-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="f216f-113">**Add-AzureRmContainerServiceAgentPoolProfile** lägger till en profil som har namnet AgentPool01 och har angivna egenskaper.</span><span class="sxs-lookup"><span data-stu-id="f216f-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="f216f-114">Kommandot skickar resultatet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f216f-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="f216f-115">Den aktuella cmdleten uppdaterar behållar tjänsten för att återspegla de ändringar som gjorts i det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="f216f-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="f216f-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f216f-116">PARAMETERS</span></span>

### <span data-ttu-id="f216f-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="f216f-117">-ContainerService</span></span>
<span data-ttu-id="f216f-118">Anger ett lokalt **ContainerService** -objekt som innehåller ändringar.</span><span class="sxs-lookup"><span data-stu-id="f216f-118">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f216f-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="f216f-119">-Name</span></span>
<span data-ttu-id="f216f-120">Anger namnet på den behållar tjänst som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="f216f-120">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f216f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f216f-121">-ResourceGroupName</span></span>
<span data-ttu-id="f216f-122">Anger resurs gruppen för den behållar tjänst som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="f216f-122">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f216f-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f216f-123">-Confirm</span></span>
<span data-ttu-id="f216f-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f216f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f216f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f216f-125">-WhatIf</span></span>
<span data-ttu-id="f216f-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f216f-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f216f-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f216f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f216f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f216f-128">CommonParameters</span></span>
<span data-ttu-id="f216f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f216f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f216f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f216f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f216f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f216f-131">INPUTS</span></span>

### <span data-ttu-id="f216f-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="f216f-132">None</span></span>
<span data-ttu-id="f216f-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f216f-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f216f-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f216f-134">OUTPUTS</span></span>

## <span data-ttu-id="f216f-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f216f-135">NOTES</span></span>

## <span data-ttu-id="f216f-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f216f-136">RELATED LINKS</span></span>

[<span data-ttu-id="f216f-137">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f216f-137">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="f216f-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f216f-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="f216f-139">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f216f-139">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="f216f-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="f216f-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="f216f-141">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f216f-141">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


