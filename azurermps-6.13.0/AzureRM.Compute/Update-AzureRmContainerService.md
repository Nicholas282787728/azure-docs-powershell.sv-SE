---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: bacc9366292225e07fd07ac65726018f1d1879e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573990"
---
# <span data-ttu-id="780ad-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="780ad-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="780ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="780ad-102">SYNOPSIS</span></span>
<span data-ttu-id="780ad-103">Uppdaterar tillståndet för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="780ad-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="780ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="780ad-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="780ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="780ad-105">DESCRIPTION</span></span>
<span data-ttu-id="780ad-106">Cmdleten **Update-AzureRmContainerService** uppdaterar statusen för en behållar tjänst så att den matchar en lokal instans av tjänsten.</span><span class="sxs-lookup"><span data-stu-id="780ad-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="780ad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="780ad-107">EXAMPLES</span></span>

### <span data-ttu-id="780ad-108">Exempel 1: uppdatera en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="780ad-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="780ad-109">Med det här kommandot hämtas behållar tjänsten med namnet CSResourceGroup17 med hjälp av Get-AzureRmContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="780ad-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="780ad-110">Kommandot skickar detta objekt till Remove-AzureRmContainerServiceAgentPoolProfile cmdlet med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="780ad-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="780ad-111">**Remove-AzureRmContainerServiceAgentPoolProfile** tar bort profilen med namnet AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="780ad-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="780ad-112">Kommandot skickar resultatet till Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="780ad-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="780ad-113">**Add-AzureRmContainerServiceAgentPoolProfile** lägger till en profil som har namnet AgentPool01 och har angivna egenskaper.</span><span class="sxs-lookup"><span data-stu-id="780ad-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="780ad-114">Kommandot skickar resultatet till den aktuella cmdleten.</span><span class="sxs-lookup"><span data-stu-id="780ad-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="780ad-115">Den aktuella cmdleten uppdaterar behållar tjänsten för att återspegla de ändringar som gjorts i det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="780ad-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="780ad-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="780ad-116">PARAMETERS</span></span>

### <span data-ttu-id="780ad-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="780ad-117">-AsJob</span></span>
<span data-ttu-id="780ad-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="780ad-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="780ad-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="780ad-119">-ContainerService</span></span>
<span data-ttu-id="780ad-120">Anger ett lokalt **ContainerService** -objekt som innehåller ändringar.</span><span class="sxs-lookup"><span data-stu-id="780ad-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="780ad-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="780ad-121">-DefaultProfile</span></span>
<span data-ttu-id="780ad-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="780ad-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="780ad-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="780ad-123">-Name</span></span>
<span data-ttu-id="780ad-124">Anger namnet på den behållar tjänst som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="780ad-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="780ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="780ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="780ad-126">Anger resurs gruppen för den behållar tjänst som denna cmdlet uppdaterar.</span><span class="sxs-lookup"><span data-stu-id="780ad-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="780ad-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="780ad-127">-Confirm</span></span>
<span data-ttu-id="780ad-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="780ad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="780ad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="780ad-129">-WhatIf</span></span>
<span data-ttu-id="780ad-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="780ad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="780ad-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="780ad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="780ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="780ad-132">CommonParameters</span></span>
<span data-ttu-id="780ad-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="780ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="780ad-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="780ad-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="780ad-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="780ad-135">INPUTS</span></span>

### <span data-ttu-id="780ad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="780ad-136">System.String</span></span>

### <span data-ttu-id="780ad-137">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="780ad-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>
<span data-ttu-id="780ad-138">Parametrar: ContainerService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="780ad-138">Parameters: ContainerService (ByValue)</span></span>

## <span data-ttu-id="780ad-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="780ad-139">OUTPUTS</span></span>

### <span data-ttu-id="780ad-140">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="780ad-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="780ad-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="780ad-141">NOTES</span></span>

## <span data-ttu-id="780ad-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="780ad-142">RELATED LINKS</span></span>

[<span data-ttu-id="780ad-143">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="780ad-143">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="780ad-144">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="780ad-144">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="780ad-145">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="780ad-145">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="780ad-146">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="780ad-146">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="780ad-147">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="780ad-147">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


