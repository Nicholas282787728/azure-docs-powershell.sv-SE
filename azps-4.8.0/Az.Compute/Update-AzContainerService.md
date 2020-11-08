---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260123"
---
# <span data-ttu-id="29e8c-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="29e8c-101">Update-AzContainerService</span></span>

## <span data-ttu-id="29e8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="29e8c-103">Uppdaterar tillståndet för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="29e8c-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="29e8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29e8c-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29e8c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="29e8c-106">Cmdleten **Update-AzContainerService** uppdaterar statusen för en behållar tjänst så att den matchar en lokal instans av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="29e8c-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="29e8c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29e8c-107">EXAMPLES</span></span>

### <span data-ttu-id="29e8c-108">Exempel 1: uppdatera en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="29e8c-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="29e8c-109">Med det här kommandot hämtas behållar tjänsten med namnet CSResourceGroup17 med hjälp av Get-AzContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29e8c-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="29e8c-110">Kommandot skickar detta objekt till Remove-AzContainerServiceAgentPoolProfile cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="29e8c-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="29e8c-111">**Remove-AzContainerServiceAgentPoolProfile** tar bort profilen med namnet AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="29e8c-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="29e8c-112">Kommandot skickar resultatet till Add-AzContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29e8c-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="29e8c-113">**Add-AzContainerServiceAgentPoolProfile** lägger till en profil som har namnet AgentPool01 och har angivna egenskaper.</span><span class="sxs-lookup"><span data-stu-id="29e8c-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="29e8c-114">Kommandot skickar resultatet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29e8c-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="29e8c-115">Den aktuella cmdleten uppdaterar behållar tjänsten för att återspegla de ändringar som gjorts i det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="29e8c-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="29e8c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29e8c-116">PARAMETERS</span></span>

### <span data-ttu-id="29e8c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29e8c-117">-AsJob</span></span>
<span data-ttu-id="29e8c-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="29e8c-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29e8c-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="29e8c-119">-ContainerService</span></span>
<span data-ttu-id="29e8c-120">Anger ett lokalt **ContainerService** -objekt som innehåller ändringar.</span><span class="sxs-lookup"><span data-stu-id="29e8c-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29e8c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29e8c-121">-DefaultProfile</span></span>
<span data-ttu-id="29e8c-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29e8c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29e8c-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="29e8c-123">-Name</span></span>
<span data-ttu-id="29e8c-124">Anger namnet på den behållar tjänst som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="29e8c-124">Specifies the name of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="29e8c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29e8c-125">-ResourceGroupName</span></span>
<span data-ttu-id="29e8c-126">Anger resurs gruppen för den behållar tjänst som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="29e8c-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="29e8c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29e8c-127">-Confirm</span></span>
<span data-ttu-id="29e8c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29e8c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29e8c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29e8c-129">-WhatIf</span></span>
<span data-ttu-id="29e8c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29e8c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29e8c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29e8c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29e8c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29e8c-132">CommonParameters</span></span>
<span data-ttu-id="29e8c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29e8c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29e8c-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29e8c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29e8c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29e8c-135">INPUTS</span></span>

### <span data-ttu-id="29e8c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="29e8c-136">System.String</span></span>

### <span data-ttu-id="29e8c-137">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="29e8c-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="29e8c-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29e8c-138">OUTPUTS</span></span>

### <span data-ttu-id="29e8c-139">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="29e8c-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="29e8c-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29e8c-140">NOTES</span></span>

## <span data-ttu-id="29e8c-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29e8c-141">RELATED LINKS</span></span>

[<span data-ttu-id="29e8c-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="29e8c-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="29e8c-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="29e8c-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="29e8c-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="29e8c-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="29e8c-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="29e8c-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="29e8c-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="29e8c-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


