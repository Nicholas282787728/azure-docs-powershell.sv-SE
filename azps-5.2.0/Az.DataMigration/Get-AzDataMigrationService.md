---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationService.md
ms.openlocfilehash: 287e4db59ae19efec604da9b63958b5ea74b747f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390033"
---
# <span data-ttu-id="f8485-101">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f8485-101">Get-AzDataMigrationService</span></span>

## <span data-ttu-id="f8485-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8485-102">SYNOPSIS</span></span>
<span data-ttu-id="f8485-103">Hämtar egenskaperna som är kopplade till en instans av Azure Database migration service.</span><span class="sxs-lookup"><span data-stu-id="f8485-103">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

## <span data-ttu-id="f8485-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8485-104">SYNTAX</span></span>

### <span data-ttu-id="f8485-105">ResourceGroupSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f8485-105">ResourceGroupSet (Default)</span></span>
```
Get-AzDataMigrationService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8485-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8485-106">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8485-107">ServiceNameGroupSet</span><span class="sxs-lookup"><span data-stu-id="f8485-107">ServiceNameGroupSet</span></span>
```
Get-AzDataMigrationService [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8485-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8485-108">DESCRIPTION</span></span>
<span data-ttu-id="f8485-109">Den Get-AzDataMigrationService cmdleten hämtar egenskaperna som är kopplade till en instans av Azure Database migration service baserat på tjänst namn och Azure Resource Group-namn som indataparametrar.</span><span class="sxs-lookup"><span data-stu-id="f8485-109">The Get-AzDataMigrationService cmdlet retrieves the properties associated with an instance of the Azure Database Migration Service based on Service name and Azure Resource Group name as input parameters.</span></span> 

## <span data-ttu-id="f8485-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8485-110">EXAMPLES</span></span>

### <span data-ttu-id="f8485-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f8485-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup -Name testService
```

<span data-ttu-id="f8485-112">Exemplet ovan hämtar egenskaperna för Azure Database migration service instans med namnet testService.</span><span class="sxs-lookup"><span data-stu-id="f8485-112">The above example retrieves the properties of the Azure Database Migration Service instance called testService.</span></span> 

### <span data-ttu-id="f8485-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f8485-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationService -ResourceGroupName testResourceGroup
```

<span data-ttu-id="f8485-114">Exemplet ovan hämtar Azure Database migration Services i resurs gruppen testResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f8485-114">The above example retrieves Azure Database Migration Services in the resource group called testResourceGroup.</span></span> 

## <span data-ttu-id="f8485-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8485-115">PARAMETERS</span></span>

### <span data-ttu-id="f8485-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8485-116">-DefaultProfile</span></span>
<span data-ttu-id="f8485-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8485-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8485-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8485-118">-Name</span></span>
<span data-ttu-id="f8485-119">Namn på databasens migreringstjänster.</span><span class="sxs-lookup"><span data-stu-id="f8485-119">Name of Database Migration Service.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases: ServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8485-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8485-120">-ResourceGroupName</span></span>
<span data-ttu-id="f8485-121">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8485-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServiceNameGroupSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8485-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8485-122">-ResourceId</span></span>
<span data-ttu-id="f8485-123">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f8485-123">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8485-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8485-124">CommonParameters</span></span>
<span data-ttu-id="f8485-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8485-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8485-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8485-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8485-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8485-127">INPUTS</span></span>

### <span data-ttu-id="f8485-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f8485-128">System.String</span></span>

## <span data-ttu-id="f8485-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8485-129">OUTPUTS</span></span>

### <span data-ttu-id="f8485-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f8485-130">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="f8485-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8485-131">NOTES</span></span>

## <span data-ttu-id="f8485-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8485-132">RELATED LINKS</span></span>
