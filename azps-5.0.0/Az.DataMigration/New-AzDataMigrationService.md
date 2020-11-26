---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320411"
---
# <span data-ttu-id="3981e-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3981e-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="3981e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3981e-102">SYNOPSIS</span></span>
<span data-ttu-id="3981e-103">Skapar en ny instans av Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="3981e-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="3981e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3981e-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3981e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3981e-105">DESCRIPTION</span></span>
<span data-ttu-id="3981e-106">New-AzDataMigrationService-cmdleten skapar en ny instans av Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="3981e-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="3981e-107">Denna cmdlet tar upp namnet på den befintliga Azure Resource-gruppen, det unika namnet på den nya instansen av Azure Database migration service som ska skapas, den region där instansen är etablerad, namnet på DMS Worker-SKU och namnet på det virtuella Azure-undernät där tjänsten ska lagras.</span><span class="sxs-lookup"><span data-stu-id="3981e-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="3981e-108">Det finns ingen parameter för prenumerations namn, eftersom det förväntas för användaren att ange standard abonnemang för Azure-inloggningssessionen eller köra Get-AzSubscription-SubscriptionName "min prenumeration" | Select-AzSubscription för att välja ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="3981e-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="3981e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3981e-109">EXAMPLES</span></span>

### <span data-ttu-id="3981e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3981e-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="3981e-111">Det här exemplet visar hur du skapar en ny instans av Azure Database migration service med namnet TestService i området Central USA.</span><span class="sxs-lookup"><span data-stu-id="3981e-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="3981e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3981e-112">PARAMETERS</span></span>

### <span data-ttu-id="3981e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3981e-113">-DefaultProfile</span></span>
<span data-ttu-id="3981e-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3981e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3981e-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="3981e-115">-Location</span></span>
<span data-ttu-id="3981e-116">Platsen för Azure Database migration service-instansen som ska skapas, som motsvarar ett Azure-område.</span><span class="sxs-lookup"><span data-stu-id="3981e-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3981e-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3981e-117">-Name</span></span>
<span data-ttu-id="3981e-118">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="3981e-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3981e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3981e-119">-ResourceGroupName</span></span>
<span data-ttu-id="3981e-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3981e-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3981e-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="3981e-121">-Sku</span></span>
<span data-ttu-id="3981e-122">SKU för Azure Database migration service instans.</span><span class="sxs-lookup"><span data-stu-id="3981e-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="3981e-123">Möjliga värden är Basic_1vCore Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="3981e-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3981e-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="3981e-124">-VirtualSubnetId</span></span>
<span data-ttu-id="3981e-125">Namnet på under nätet under det virtuella nätverk som ska användas för Azure Database migration service instans.</span><span class="sxs-lookup"><span data-stu-id="3981e-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3981e-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3981e-126">-Confirm</span></span>
<span data-ttu-id="3981e-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3981e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3981e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3981e-128">-WhatIf</span></span>
<span data-ttu-id="3981e-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3981e-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3981e-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3981e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3981e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3981e-131">CommonParameters</span></span>
<span data-ttu-id="3981e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3981e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3981e-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3981e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3981e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3981e-134">INPUTS</span></span>

### <span data-ttu-id="3981e-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="3981e-135">None</span></span>

## <span data-ttu-id="3981e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3981e-136">OUTPUTS</span></span>

### <span data-ttu-id="3981e-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="3981e-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="3981e-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3981e-138">NOTES</span></span>

## <span data-ttu-id="3981e-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3981e-139">RELATED LINKS</span></span>