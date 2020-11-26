---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260023"
---
# <span data-ttu-id="73505-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="73505-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="73505-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73505-102">SYNOPSIS</span></span>
<span data-ttu-id="73505-103">Hämtar egenskaperna för ett Azure Database migration Project.</span><span class="sxs-lookup"><span data-stu-id="73505-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="73505-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73505-104">SYNTAX</span></span>

### <span data-ttu-id="73505-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="73505-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73505-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73505-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73505-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73505-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73505-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73505-108">DESCRIPTION</span></span>
<span data-ttu-id="73505-109">Get-AzDataMigrationProject cmdlet hämtar egenskaperna för ett Azure Database migration Project.</span><span class="sxs-lookup"><span data-stu-id="73505-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="73505-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73505-110">EXAMPLES</span></span>

### <span data-ttu-id="73505-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73505-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="73505-112">Exemplet ovan hämtar ett Azure Database migration-projekt med namnet TestProject i resurs gruppen som heter testResourceGroup och under tjänst heter testService</span><span class="sxs-lookup"><span data-stu-id="73505-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="73505-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="73505-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="73505-114">Exemplet ovan hämtar Azure Database migration Project baserat på PSProject-indataparameter som skickades.</span><span class="sxs-lookup"><span data-stu-id="73505-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="73505-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73505-115">PARAMETERS</span></span>

### <span data-ttu-id="73505-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73505-116">-DefaultProfile</span></span>
<span data-ttu-id="73505-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73505-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73505-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73505-118">-InputObject</span></span>
<span data-ttu-id="73505-119">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="73505-119">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73505-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="73505-120">-Name</span></span>
<span data-ttu-id="73505-121">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="73505-121">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73505-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73505-122">-ResourceGroupName</span></span>
<span data-ttu-id="73505-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="73505-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73505-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73505-124">-ResourceId</span></span>
<span data-ttu-id="73505-125">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="73505-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="73505-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="73505-126">-ServiceName</span></span>
<span data-ttu-id="73505-127">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="73505-127">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73505-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73505-128">CommonParameters</span></span>
<span data-ttu-id="73505-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73505-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73505-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73505-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73505-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73505-131">INPUTS</span></span>

### <span data-ttu-id="73505-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="73505-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="73505-133">System. String</span><span class="sxs-lookup"><span data-stu-id="73505-133">System.String</span></span>

## <span data-ttu-id="73505-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73505-134">OUTPUTS</span></span>

### <span data-ttu-id="73505-135">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="73505-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="73505-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73505-136">NOTES</span></span>

## <span data-ttu-id="73505-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73505-137">RELATED LINKS</span></span>