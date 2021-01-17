---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Get-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Get-AzDataMigrationProject.md
ms.openlocfilehash: 7fe1e12c7c7feb2a47ac33b309b188e53e77fc73
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390042"
---
# <span data-ttu-id="d4714-101">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="d4714-101">Get-AzDataMigrationProject</span></span>

## <span data-ttu-id="d4714-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4714-102">SYNOPSIS</span></span>
<span data-ttu-id="d4714-103">Hämtar egenskaperna för ett Azure Database migration Project.</span><span class="sxs-lookup"><span data-stu-id="d4714-103">Retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="d4714-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4714-104">SYNTAX</span></span>

### <span data-ttu-id="d4714-105">ComponentNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d4714-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4714-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4714-106">ComponentObjectParameterSet</span></span>
```
Get-AzDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4714-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4714-107">ResourceIdParameterSet</span></span>
```
Get-AzDataMigrationProject [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4714-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4714-108">DESCRIPTION</span></span>
<span data-ttu-id="d4714-109">Get-AzDataMigrationProject cmdlet hämtar egenskaperna för ett Azure Database migration Project.</span><span class="sxs-lookup"><span data-stu-id="d4714-109">The Get-AzDataMigrationProject cmdlet retrieves the properties of an Azure Database Migration project.</span></span>

## <span data-ttu-id="d4714-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4714-110">EXAMPLES</span></span>

### <span data-ttu-id="d4714-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4714-111">Example 1</span></span>
```
PS C:\> Get-AzDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

<span data-ttu-id="d4714-112">Exemplet ovan hämtar ett Azure Database migration-projekt med namnet TestProject i resurs gruppen som heter testResourceGroup och under tjänst heter testService</span><span class="sxs-lookup"><span data-stu-id="d4714-112">The above example retrieves  Azure Database Migration project named TestProject in the resource group called testResourceGroup and under service called testService</span></span>

### <span data-ttu-id="d4714-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d4714-113">Example 2</span></span>
```
PS C:\> Get-AzDataMigrationProject -InputObject $myService
```

<span data-ttu-id="d4714-114">Exemplet ovan hämtar Azure Database migration Project baserat på PSProject-indataparameter som skickades.</span><span class="sxs-lookup"><span data-stu-id="d4714-114">The above example retrieves the  Azure Database Migration project based on PSProject object input parameter passed in.</span></span> 

## <span data-ttu-id="d4714-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4714-115">PARAMETERS</span></span>

### <span data-ttu-id="d4714-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4714-116">-DefaultProfile</span></span>
<span data-ttu-id="d4714-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4714-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4714-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4714-118">-InputObject</span></span>
<span data-ttu-id="d4714-119">PSDataMigrationService-objekt.</span><span class="sxs-lookup"><span data-stu-id="d4714-119">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="d4714-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4714-120">-Name</span></span>
<span data-ttu-id="d4714-121">Namnet på projektet.</span><span class="sxs-lookup"><span data-stu-id="d4714-121">The name of the project.</span></span>

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

### <span data-ttu-id="d4714-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4714-122">-ResourceGroupName</span></span>
<span data-ttu-id="d4714-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d4714-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4714-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4714-124">-ResourceId</span></span>
<span data-ttu-id="d4714-125">DataMigrationService resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d4714-125">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="d4714-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d4714-126">-ServiceName</span></span>
<span data-ttu-id="d4714-127">Tjänst namn för databas migration.</span><span class="sxs-lookup"><span data-stu-id="d4714-127">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="d4714-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4714-128">CommonParameters</span></span>
<span data-ttu-id="d4714-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4714-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4714-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4714-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4714-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4714-131">INPUTS</span></span>

### <span data-ttu-id="d4714-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d4714-132">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="d4714-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d4714-133">System.String</span></span>

## <span data-ttu-id="d4714-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4714-134">OUTPUTS</span></span>

### <span data-ttu-id="d4714-135">Microsoft. Azure. commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="d4714-135">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="d4714-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4714-136">NOTES</span></span>

## <span data-ttu-id="d4714-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4714-137">RELATED LINKS</span></span>
