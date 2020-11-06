---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: cc2f708294be05b16b0c5be94fb9da260b479799
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580119"
---
# <span data-ttu-id="ccd20-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ccd20-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="ccd20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ccd20-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd20-103">Skapar en ny instans av Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="ccd20-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccd20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ccd20-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccd20-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ccd20-105">DESCRIPTION</span></span>
<span data-ttu-id="ccd20-106">New-AzureRmDataMigrationService-cmdleten skapar en ny instans av Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="ccd20-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="ccd20-107">Denna cmdlet tar upp namnet på den befintliga Azure Resource-gruppen, det unika namnet på den nya instansen av Azure Database migration service som ska skapas, den region där instansen är etablerad, namnet på DMS Worker-SKU och namnet på det virtuella Azure-undernät där tjänsten ska lagras.</span><span class="sxs-lookup"><span data-stu-id="ccd20-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="ccd20-108">Det finns ingen parameter för prenumerations namn, eftersom det förväntas för användaren att ange standard abonnemang för Azure-inloggningssessionen eller köra Get-AzureRmSubscription-SubscriptionName "min prenumeration" | Select-AzureRmSubscription för att välja ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="ccd20-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription -SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="ccd20-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ccd20-109">EXAMPLES</span></span>

### <span data-ttu-id="ccd20-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ccd20-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="ccd20-111">Det här exemplet visar hur du skapar en ny instans av Azure Database migration service med namnet TestService i området Central USA.</span><span class="sxs-lookup"><span data-stu-id="ccd20-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="ccd20-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ccd20-112">PARAMETERS</span></span>

### <span data-ttu-id="ccd20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd20-113">-DefaultProfile</span></span>
<span data-ttu-id="ccd20-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ccd20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccd20-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="ccd20-115">-Location</span></span>
<span data-ttu-id="ccd20-116">Platsen för Azure Database migration service-instansen som ska skapas, som motsvarar ett Azure-område.</span><span class="sxs-lookup"><span data-stu-id="ccd20-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="ccd20-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="ccd20-117">-Name</span></span>
<span data-ttu-id="ccd20-118">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="ccd20-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="ccd20-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccd20-119">-ResourceGroupName</span></span>
<span data-ttu-id="ccd20-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ccd20-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="ccd20-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="ccd20-121">-Sku</span></span>
<span data-ttu-id="ccd20-122">SKU för Azure Database migration service instans.</span><span class="sxs-lookup"><span data-stu-id="ccd20-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="ccd20-123">Möjliga värden är Basic_1vCore Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="ccd20-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="ccd20-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="ccd20-124">-VirtualSubnetId</span></span>
<span data-ttu-id="ccd20-125">Namnet på under nätet under det virtuella nätverk som ska användas för Azure Database migration service instans.</span><span class="sxs-lookup"><span data-stu-id="ccd20-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="ccd20-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ccd20-126">-Confirm</span></span>
<span data-ttu-id="ccd20-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ccd20-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccd20-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccd20-128">-WhatIf</span></span>
<span data-ttu-id="ccd20-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ccd20-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ccd20-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ccd20-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccd20-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd20-131">CommonParameters</span></span>
<span data-ttu-id="ccd20-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccd20-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd20-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccd20-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd20-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ccd20-134">INPUTS</span></span>

### <span data-ttu-id="ccd20-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="ccd20-135">None</span></span>

## <span data-ttu-id="ccd20-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ccd20-136">OUTPUTS</span></span>

### <span data-ttu-id="ccd20-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="ccd20-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="ccd20-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ccd20-138">NOTES</span></span>

## <span data-ttu-id="ccd20-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ccd20-139">RELATED LINKS</span></span>
