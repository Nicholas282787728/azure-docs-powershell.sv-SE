---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: a89494b155755cf716f39275debcfb7477071da2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930369"
---
# <span data-ttu-id="4f3c3-101">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="4f3c3-101">Add-AzureRmContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="4f3c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f3c3-102">SYNOPSIS</span></span>
<span data-ttu-id="4f3c3-103">Lägger till en cacheprofil för en behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-103">Adds a container service agent pool profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f3c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f3c3-104">SYNTAX</span></span>

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f3c3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f3c3-105">DESCRIPTION</span></span>
<span data-ttu-id="4f3c3-106">Cmdleten **Add-AzureRmContainerServiceAgentPoolProfile** lägger till en programpool för behållar tjänst till ett objekt för lokal behållar tjänst.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-106">The **Add-AzureRmContainerServiceAgentPoolProfile** cmdlet adds a container service agent pool profile to a local container service object.</span></span>

## <span data-ttu-id="4f3c3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f3c3-107">EXAMPLES</span></span>

### <span data-ttu-id="4f3c3-108">Exempel 1: lägga till en profil</span><span class="sxs-lookup"><span data-stu-id="4f3c3-108">Example 1: Add a profile</span></span>
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="4f3c3-109">Det här kommandot lägger till en behållare för en programpool i det lokala behållarobjekts tjänstens objekt.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-109">This command adds a container service agent pool profile to the local container service object.</span></span>

## <span data-ttu-id="4f3c3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f3c3-110">PARAMETERS</span></span>

### <span data-ttu-id="4f3c3-111">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="4f3c3-111">-ContainerService</span></span>
<span data-ttu-id="4f3c3-112">Anger det behållar tjänst objekt som denna cmdlet lägger till en cacheprofil för.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-112">Specifies the container service object to which this cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="4f3c3-113">För att få ett **ContainerService** -objekt, Använd cmdleten [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="4f3c3-113">To obtain a **ContainerService** object, use the [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="4f3c3-114">-Antal</span><span class="sxs-lookup"><span data-stu-id="4f3c3-114">-Count</span></span>
<span data-ttu-id="4f3c3-115">Anger antalet agenter som är värd för behållarna.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-115">Specifies the number of agents that host containers.</span></span>
<span data-ttu-id="4f3c3-116">De acceptabla värdena för den här parametern är: heltal från 1 till 100.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-116">The acceptable values for this parameter are: integers from 1 to 100.</span></span>
<span data-ttu-id="4f3c3-117">Standardvärdet är 1.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-117">The default value is 1.</span></span>

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

### <span data-ttu-id="4f3c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f3c3-118">-DefaultProfile</span></span>
<span data-ttu-id="4f3c3-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f3c3-120">-DnsPrefix</span><span class="sxs-lookup"><span data-stu-id="4f3c3-120">-DnsPrefix</span></span>
<span data-ttu-id="4f3c3-121">Anger det DNS-prefix som denna cmdlet använder för att skapa det fullständigt kvalificerade domän namnet för den här poolen.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-121">Specifies the DNS prefix that this cmdlet uses to create the fully qualified domain name for this agent pool.</span></span>

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

### <span data-ttu-id="4f3c3-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4f3c3-122">-Name</span></span>
<span data-ttu-id="4f3c3-123">Anger namnet på mediepoolen.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-123">Specifies the name of the agent pool profile.</span></span>
<span data-ttu-id="4f3c3-124">Det här värdet måste vara unikt i kontexten för abonnemanget och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-124">This value must be unique in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="4f3c3-125">-VmSize</span><span class="sxs-lookup"><span data-stu-id="4f3c3-125">-VmSize</span></span>
<span data-ttu-id="4f3c3-126">Anger storleken på de virtuella datorerna för agenterna.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-126">Specifies the size of the virtual machines for the agents.</span></span>

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

### <span data-ttu-id="4f3c3-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f3c3-127">-Confirm</span></span>
<span data-ttu-id="4f3c3-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f3c3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f3c3-129">-WhatIf</span></span>
<span data-ttu-id="4f3c3-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f3c3-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f3c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f3c3-132">CommonParameters</span></span>
<span data-ttu-id="4f3c3-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f3c3-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f3c3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f3c3-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f3c3-135">INPUTS</span></span>

### <span data-ttu-id="4f3c3-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="4f3c3-136">ContainerService</span></span>
<span data-ttu-id="4f3c3-137">Parametern ' ContainerService ' godkänner värdet av typen ' ContainerService ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="4f3c3-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="4f3c3-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f3c3-138">OUTPUTS</span></span>

### <span data-ttu-id="4f3c3-139">Microsoft. Azure. commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="4f3c3-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="4f3c3-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f3c3-140">NOTES</span></span>

## <span data-ttu-id="4f3c3-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f3c3-141">RELATED LINKS</span></span>

[<span data-ttu-id="4f3c3-142">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="4f3c3-142">New-AzureRmContainerServiceConfig</span></span>](./New-AzureRmContainerServiceConfig.md)

[<span data-ttu-id="4f3c3-143">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="4f3c3-143">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
