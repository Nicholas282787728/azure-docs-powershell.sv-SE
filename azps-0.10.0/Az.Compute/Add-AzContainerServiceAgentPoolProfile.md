---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: c1a3cf88350c02359633d73b074ea1faa910bde9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93921957"
---
# <span data-ttu-id="7e6e2-101">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7e6e2-101">Add-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="7e6e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="7e6e2-103">Lägger till en cacheprofil för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-103">Adds a container service agent pool profile.</span></span>

## <span data-ttu-id="7e6e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e6e2-104">SYNTAX</span></span>

```
Add-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e6e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e6e2-105">DESCRIPTION</span></span>
<span data-ttu-id="7e6e2-106">Cmdleten **Add-AzContainerServiceAgentPoolProfile** lägger till en programpool för behållar tjänst till ett objekt för lokal behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-106">The **Add-AzContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="7e6e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e6e2-107">EXAMPLES</span></span>

### <span data-ttu-id="7e6e2-108">Exempel 1: lägga till en profil</span><span class="sxs-lookup"><span data-stu-id="7e6e2-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="7e6e2-109">Det här kommandot lägger till en behållare för en programpool i det lokala behållarobjekts tjänstens objekt.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="7e6e2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e6e2-110">PARAMETERS</span></span>

### <span data-ttu-id="7e6e2-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="7e6e2-111">-ContainerService</span></span>
<span data-ttu-id="7e6e2-112">Anger det behållar tjänst objekt som denna cmdlet lägger till en cacheprofil för.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="7e6e2-113">För att få ett **ContainerService** -objekt, Använd cmdleten [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="7e6e2-113">To obtain a **ContainerService** object, use the [New-AzContainerServiceConfig](./New-AzContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="7e6e2-114">-Antal</span><span class="sxs-lookup"><span data-stu-id="7e6e2-114">-Count</span></span>
<span data-ttu-id="7e6e2-115">Anger antalet agenter som är värd för behållarna.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="7e6e2-116">De acceptabla värdena för den här parametern är: heltal från 1 till 100.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="7e6e2-117">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-117">The default value is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e6e2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e6e2-118">-DefaultProfile</span></span>
<span data-ttu-id="7e6e2-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e6e2-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="7e6e2-120">-DnsPrefix</span></span>
<span data-ttu-id="7e6e2-121">Anger det DNS-prefix som denna cmdlet använder för att skapa det fullständigt kvalificerade domän namnet för den här poolen.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e6e2-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e6e2-122">-Name</span></span>
<span data-ttu-id="7e6e2-123">Anger namnet på mediepoolen.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="7e6e2-124">Det här värdet måste vara unikt i kontexten för abonnemanget och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-124">This value must be unique in the context of the subscription and resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e6e2-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="7e6e2-125">-VmSize</span></span>
<span data-ttu-id="7e6e2-126">Anger storleken på de virtuella datorerna för agenterna.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-126">Specifies the size of the virtual machines for the agents.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e6e2-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7e6e2-127">-Confirm</span></span>
<span data-ttu-id="7e6e2-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e6e2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e6e2-129">-WhatIf</span></span>
<span data-ttu-id="7e6e2-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e6e2-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e6e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e6e2-132">CommonParameters</span></span>
<span data-ttu-id="7e6e2-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e6e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e6e2-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e6e2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e6e2-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e6e2-135">INPUTS</span></span>

### <span data-ttu-id="7e6e2-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="7e6e2-136">ContainerService</span></span>
<span data-ttu-id="7e6e2-137">Parametern ' ContainerService ' godkänner värdet av typen ' ContainerService ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="7e6e2-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="7e6e2-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e6e2-138">OUTPUTS</span></span>

### <span data-ttu-id="7e6e2-139">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="7e6e2-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="7e6e2-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e6e2-140">NOTES</span></span>

## <span data-ttu-id="7e6e2-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e6e2-141">RELATED LINKS</span></span>

[<span data-ttu-id="7e6e2-142">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="7e6e2-142">New-AzContainerServiceConfig</span></span>](./New-AzContainerServiceConfig.md)

[<span data-ttu-id="7e6e2-143">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="7e6e2-143">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)
