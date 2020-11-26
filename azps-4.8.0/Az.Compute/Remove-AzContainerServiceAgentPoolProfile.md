---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103033"
---
# <span data-ttu-id="e9e9c-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e9e9c-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="e9e9c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e9c-103">Tar bort en cacheprofil från en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="e9e9c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9e9c-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9e9c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9e9c-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e9c-106">Cmdleten **Remove-AzContainerServiceAgentPoolProfile** tar bort en cacheprofil för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="e9e9c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9e9c-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e9c-108">Exempel 1: ta bort en profil från en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="e9e9c-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="e9e9c-109">Det första kommandot får en behållar tjänst med namnet CSResourceGroup17 med hjälp av Get-AzContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="e9e9c-110">Kommandot sparar tjänsten i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="e9e9c-111">Det andra kommandot tar bort den profil som heter AgentPool01 från behållar tjänsten i $Container.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="e9e9c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9e9c-112">PARAMETERS</span></span>

### <span data-ttu-id="e9e9c-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="e9e9c-113">-ContainerService</span></span>
<span data-ttu-id="e9e9c-114">Anger det behållar tjänst objekt som den här cmdleten tar bort en cacheprofil för.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9e9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e9c-115">-DefaultProfile</span></span>
<span data-ttu-id="e9e9c-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9e9c-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="e9e9c-117">-Name</span></span>
<span data-ttu-id="e9e9c-118">Anger namnet på den cacheprofil som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e9e9c-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e9e9c-119">-Confirm</span></span>
<span data-ttu-id="e9e9c-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e9c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e9c-121">-WhatIf</span></span>
<span data-ttu-id="e9e9c-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9e9c-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e9c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e9c-124">CommonParameters</span></span>
<span data-ttu-id="e9e9c-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e9c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e9c-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9e9c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e9c-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9e9c-127">INPUTS</span></span>

### <span data-ttu-id="e9e9c-128">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e9e9c-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="e9e9c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e9e9c-129">System.String</span></span>

## <span data-ttu-id="e9e9c-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9e9c-130">OUTPUTS</span></span>

### <span data-ttu-id="e9e9c-131">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="e9e9c-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="e9e9c-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9e9c-132">NOTES</span></span>

## <span data-ttu-id="e9e9c-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9e9c-133">RELATED LINKS</span></span>

[<span data-ttu-id="e9e9c-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="e9e9c-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="e9e9c-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="e9e9c-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

