---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationService.md
ms.openlocfilehash: cac57ff34d925d553c25d97facd81dba017a25c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579544"
---
# <span data-ttu-id="1abb1-101">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="1abb1-101">Get-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="1abb1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1abb1-102">SYNOPSIS</span></span>
<span data-ttu-id="1abb1-103">Hämtar egenskaperna som är kopplade till en instans av Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="1abb1-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1abb1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1abb1-104">SYNTAX</span></span>

### <span data-ttu-id="1abb1-105">ResourceGroupSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1abb1-105">ResourceGroupSet (Default)</span></span>
```
Get-AzureRmDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="1abb1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1abb1-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="1abb1-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="1abb1-107">ServiceNameGroupSet</span></span>
```
Get-AzureRmDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>]
```
## <span data-ttu-id="1abb1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1abb1-108">DESCRIPTION</span></span>
<span data-ttu-id="1abb1-109">Den Get-AzureRmDataMigrationService cmdleten hämtar egenskaperna som är kopplade till en instans av Azure Database migration service baserat på tjänst namn och Azure Resource Group-namn som indataparametrar.</span><span class="sxs-lookup"><span data-stu-id="1abb1-109">The Get-AzureRmDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="1abb1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1abb1-110">EXAMPLES</span></span>

### <span data-ttu-id="1abb1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1abb1-111">Example 1</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="1abb1-112">Exemplet ovan hämtar egenskaperna för Azure Database migration service instans med namnet testService.</span><span class="sxs-lookup"><span data-stu-id="1abb1-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="1abb1-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="1abb1-113">Example 2</span></span>
```
PS C:\> Get-AzureRmDataMigrationService -ResourceGroupName testResourceGroup 
```

<span data-ttu-id="1abb1-114">Exemplet ovan hämtar Azure Database migration Services i resurs gruppen testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1abb1-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="1abb1-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1abb1-115">PARAMETERS</span></span>

### <span data-ttu-id="1abb1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abb1-116">-DefaultProfile</span></span>
<span data-ttu-id="1abb1-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1abb1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1abb1-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="1abb1-118">-Name</span></span>
<span data-ttu-id="1abb1-119">Namn på Datamigreringshanteraren.</span><span class="sxs-lookup"><span data-stu-id="1abb1-119">Name of Data Migration Service.</span></span>

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1abb1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1abb1-120">-ResourceGroupName</span></span>
<span data-ttu-id="1abb1-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1abb1-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServiceNameGroupSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1abb1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1abb1-122">-ResourceId</span></span>
<span data-ttu-id="1abb1-123">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1abb1-123">DataMigrationService Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="1abb1-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1abb1-124">INPUTS</span></span>

### <span data-ttu-id="1abb1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1abb1-125">System.String</span></span>


## <span data-ttu-id="1abb1-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1abb1-126">OUTPUTS</span></span>

### <span data-ttu-id="1abb1-127">System. Collections. Generic. IList ' 1 [[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft. Azure. kommandon. DataMigration, version = 0.1.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1abb1-127">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService, Microsoft.Azure.Commands.DataMigration, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="1abb1-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1abb1-128">NOTES</span></span>

## <span data-ttu-id="1abb1-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1abb1-129">RELATED LINKS</span></span>





