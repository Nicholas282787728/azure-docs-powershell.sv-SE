---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: cfcb3c7657bc0ff99646c3ef21eb5cceb592fe2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755395"
---
# <span data-ttu-id="b25ff-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b25ff-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="b25ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b25ff-102">SYNOPSIS</span></span>
<span data-ttu-id="b25ff-103">Tar bort en cacheprofil från en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="b25ff-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b25ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b25ff-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [-Name] <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b25ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b25ff-105">DESCRIPTION</span></span>
<span data-ttu-id="b25ff-106">Cmdleten **Remove-AzureRmContainerServiceAgentPoolProfile** tar bort en cacheprofil för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="b25ff-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="b25ff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b25ff-107">EXAMPLES</span></span>

### <span data-ttu-id="b25ff-108">Exempel 1: ta bort en profil från en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="b25ff-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="b25ff-109">Det första kommandot får en behållar tjänst med namnet CSResourceGroup17 med hjälp av Get-AzureRmContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b25ff-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="b25ff-110">Kommandot sparar tjänsten i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="b25ff-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="b25ff-111">Det andra kommandot tar bort den profil som heter AgentPool01 från behållar tjänsten i $Container.</span><span class="sxs-lookup"><span data-stu-id="b25ff-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="b25ff-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b25ff-112">PARAMETERS</span></span>

### <span data-ttu-id="b25ff-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="b25ff-113">-ContainerService</span></span>
<span data-ttu-id="b25ff-114">Anger det behållar tjänst objekt som den här cmdleten tar bort en cacheprofil för.</span><span class="sxs-lookup"><span data-stu-id="b25ff-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b25ff-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="b25ff-115">-Name</span></span>
<span data-ttu-id="b25ff-116">Anger namnet på den cacheprofil som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="b25ff-116">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b25ff-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b25ff-117">-Confirm</span></span>
<span data-ttu-id="b25ff-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b25ff-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25ff-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b25ff-119">-WhatIf</span></span>
<span data-ttu-id="b25ff-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b25ff-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b25ff-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b25ff-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b25ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25ff-122">CommonParameters</span></span>
<span data-ttu-id="b25ff-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b25ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25ff-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b25ff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25ff-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b25ff-125">INPUTS</span></span>

### <span data-ttu-id="b25ff-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="b25ff-126">None</span></span>
<span data-ttu-id="b25ff-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="b25ff-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b25ff-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b25ff-128">OUTPUTS</span></span>

## <span data-ttu-id="b25ff-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b25ff-129">NOTES</span></span>

## <span data-ttu-id="b25ff-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b25ff-130">RELATED LINKS</span></span>

[<span data-ttu-id="b25ff-131">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b25ff-131">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="b25ff-132">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b25ff-132">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


