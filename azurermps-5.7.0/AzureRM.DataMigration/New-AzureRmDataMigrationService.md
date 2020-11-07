---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757687"
---
# <span data-ttu-id="af69f-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="af69f-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="af69f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="af69f-102">SYNOPSIS</span></span>
<span data-ttu-id="af69f-103">Skapar en ny instans av Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="af69f-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af69f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="af69f-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="af69f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="af69f-105">DESCRIPTION</span></span>
<span data-ttu-id="af69f-106">New-AzureRmDataMigrationService-cmdleten skapar en ny instans av Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="af69f-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="af69f-107">Denna cmdlet tar upp namnet på den befintliga Azure Resource-gruppen, det unika namnet på den nya instansen av Azure Database migration service som ska skapas, den region där instansen är etablerad, namnet på DMS Worker-SKU och namnet på det virtuella Azure-undernät där tjänsten ska lagras.</span><span class="sxs-lookup"><span data-stu-id="af69f-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="af69f-108">Det finns ingen parameter för prenumerations namnet eftersom det förväntas för användaren att ange standard abonnemang för Azure-inloggningssessionen eller EXECUTE Get-AzureRmSubscription-SubscriptionName "min prenumeration" | Select-AzureRmSubscription för att välja ett annat abonnemang.</span><span class="sxs-lookup"><span data-stu-id="af69f-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription –SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="af69f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="af69f-109">EXAMPLES</span></span>

### <span data-ttu-id="af69f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="af69f-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="af69f-111">Det här exemplet visar hur du skapar en ny instans av Azure Database migration service med namnet TestService i området Central USA.</span><span class="sxs-lookup"><span data-stu-id="af69f-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>


## <span data-ttu-id="af69f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="af69f-112">PARAMETERS</span></span>

### <span data-ttu-id="af69f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af69f-113">-DefaultProfile</span></span>
<span data-ttu-id="af69f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="af69f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af69f-115">-Plats</span><span class="sxs-lookup"><span data-stu-id="af69f-115">-Location</span></span>
<span data-ttu-id="af69f-116">Platsen för Azure Database migration service-instansen som ska skapas, som motsvarar ett Azure-område.</span><span class="sxs-lookup"><span data-stu-id="af69f-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af69f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af69f-117">-ResourceGroupName</span></span>
<span data-ttu-id="af69f-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="af69f-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af69f-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="af69f-119">-ServiceName</span></span>
<span data-ttu-id="af69f-120">Namnet på instansen för Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="af69f-120">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af69f-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="af69f-121">-Sku</span></span>
<span data-ttu-id="af69f-122">SKU för Azure Database migration service instans.</span><span class="sxs-lookup"><span data-stu-id="af69f-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="af69f-123">Möjliga värden är Basic_1vCore Basic_2vCores GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="af69f-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af69f-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="af69f-124">-VirtualSubnetId</span></span>
<span data-ttu-id="af69f-125">Namnet på under nätet under det virtuella nätverk som ska användas för Azure Database migration service instans.</span><span class="sxs-lookup"><span data-stu-id="af69f-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="af69f-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="af69f-126">OUTPUTS</span></span>

### <span data-ttu-id="af69f-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="af69f-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>


## <span data-ttu-id="af69f-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="af69f-128">NOTES</span></span>

## <span data-ttu-id="af69f-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="af69f-129">RELATED LINKS</span></span>

