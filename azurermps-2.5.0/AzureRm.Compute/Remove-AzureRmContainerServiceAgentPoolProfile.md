---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930669"
---
# <span data-ttu-id="05e20-101">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="05e20-101">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="05e20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05e20-102">SYNOPSIS</span></span>
<span data-ttu-id="05e20-103">Tar bort en cacheprofil från en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="05e20-103">Removes an agent pool profile from a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05e20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05e20-104">SYNTAX</span></span>

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05e20-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05e20-105">DESCRIPTION</span></span>
<span data-ttu-id="05e20-106">Cmdleten **Remove-AzureRmContainerServiceAgentPoolProfile** tar bort en cacheprofil för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="05e20-106">The **Remove-AzureRmContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="05e20-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05e20-107">EXAMPLES</span></span>

### <span data-ttu-id="05e20-108">Exempel 1: ta bort en profil från en behållar tjänst</span><span class="sxs-lookup"><span data-stu-id="05e20-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="05e20-109">Det första kommandot får en behållar tjänst med namnet CSResourceGroup17 med hjälp av Get-AzureRmContainerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05e20-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="05e20-110">Kommandot sparar tjänsten i $Container variabel.</span><span class="sxs-lookup"><span data-stu-id="05e20-110">The command stores the service in the $Container variable.</span></span>

<span data-ttu-id="05e20-111">Det andra kommandot tar bort den profil som heter AgentPool01 från behållar tjänsten i $Container.</span><span class="sxs-lookup"><span data-stu-id="05e20-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="05e20-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05e20-112">PARAMETERS</span></span>

### <span data-ttu-id="05e20-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="05e20-113">-ContainerService</span></span>
<span data-ttu-id="05e20-114">Anger det behållar tjänst objekt som den här cmdleten tar bort en cacheprofil för.</span><span class="sxs-lookup"><span data-stu-id="05e20-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05e20-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e20-115">-DefaultProfile</span></span>
<span data-ttu-id="05e20-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05e20-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05e20-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="05e20-117">-Name</span></span>
<span data-ttu-id="05e20-118">Anger namnet på den cacheprofil som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="05e20-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="05e20-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05e20-119">-Confirm</span></span>
<span data-ttu-id="05e20-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05e20-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05e20-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05e20-121">-WhatIf</span></span>
<span data-ttu-id="05e20-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05e20-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05e20-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05e20-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05e20-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e20-124">CommonParameters</span></span>
<span data-ttu-id="05e20-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e20-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e20-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e20-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e20-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05e20-127">INPUTS</span></span>

### <span data-ttu-id="05e20-128">ContainerService</span><span class="sxs-lookup"><span data-stu-id="05e20-128">ContainerService</span></span>
<span data-ttu-id="05e20-129">Parametern ' ContainerService ' godkänner värdet av typen ' ContainerService ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="05e20-129">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="05e20-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05e20-130">OUTPUTS</span></span>

### <span data-ttu-id="05e20-131">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="05e20-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="05e20-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05e20-132">NOTES</span></span>

## <span data-ttu-id="05e20-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05e20-133">RELATED LINKS</span></span>

[<span data-ttu-id="05e20-134">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="05e20-134">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="05e20-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="05e20-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)


