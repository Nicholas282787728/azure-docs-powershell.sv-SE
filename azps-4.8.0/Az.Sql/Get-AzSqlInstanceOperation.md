---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceOperation.md
ms.openlocfilehash: a190e6a47c0a3027505c471be870c10ac80593cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260968"
---
# <span data-ttu-id="b8ff4-101">Get-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="b8ff4-101">Get-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="b8ff4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ff4-103">Hämtar SQL-hanterade instanser.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-103">Gets a SQL managed instance's operations.</span></span>

## <span data-ttu-id="b8ff4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8ff4-104">SYNTAX</span></span>

### <span data-ttu-id="b8ff4-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b8ff4-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceOperation [-Name <String>] -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8ff4-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8ff4-106">GetByManagedInstanceOperationResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstanceOperation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8ff4-107">ListByManagedInstanceParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8ff4-107">ListByManagedInstanceParameterSet</span></span>
```
Get-AzSqlInstanceOperation -ManagedInstanceName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8ff4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8ff4-108">DESCRIPTION</span></span>
<span data-ttu-id="b8ff4-109">Get-AzSqlInstanceOperation-cmdleten hämtar information om åtgärderna i en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-109">The Get-AzSqlInstanceOperation cmdlet gets information about the operations on a SQL managed instance.</span></span> <span data-ttu-id="b8ff4-110">Du kan visa alla åtgärder på en hanterad instans eller Visa en specifik åtgärd genom att ange namnet på åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-110">You can view all operations on a managed instance or view a specific operation by providing the operation name.</span></span>

## <span data-ttu-id="b8ff4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8ff4-111">EXAMPLES</span></span>

### <span data-ttu-id="b8ff4-112">Exempel 1: få alla förekomster</span><span class="sxs-lookup"><span data-stu-id="b8ff4-112">Example 1: Get all instance's operations</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/79f2c91b-0080-4c14-b9b4-d9991c6e82dd
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 79f2c91b-0080-4c14-b9b4-d9991c6e82dd
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:19:53 AM
State                   : Cancelled
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="b8ff4-113">Det här kommandot får alla operationer som en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-113">This command gets all operations a SQL managed instance.</span></span>

### <span data-ttu-id="b8ff4-114">Exempel 2: få en särskild åtgärd</span><span class="sxs-lookup"><span data-stu-id="b8ff4-114">Example 2: Get a specific operation</span></span>
```powershell
PS C:\> Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="b8ff4-115">Det här kommandot hämtar åtgärden med namnet ' 5870c6d8-6703-4b27-8ae4-687b4ca7caea ' på en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-115">This command gets operation with name '5870c6d8-6703-4b27-8ae4-687b4ca7caea' on a SQL managed instance.</span></span>

### <span data-ttu-id="b8ff4-116">Exempel 3: använda resurs-ID för operation</span><span class="sxs-lookup"><span data-stu-id="b8ff4-116">Example 3: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 5870c6d8-6703-4b27-8ae4-687b4ca7caea
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 5870c6d8-6703-4b27-8ae4-687b4ca7caea
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 100
StartTime               : 3/16/2020 8:11:13 AM
State                   : Succeeded
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : False
OperationParameters     : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationParametersPair
OperationSteps          : Microsoft.Azure.Management.Sql.Models.ManagedInstanceOperationSteps
```

<span data-ttu-id="b8ff4-117">Det här kommandot får en åtgärd med ID '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea '.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-117">This command gets operation with id '/subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/5870c6d8-6703-4b27-8ae4-687b4ca7caea'.</span></span>

## <span data-ttu-id="b8ff4-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8ff4-118">PARAMETERS</span></span>

### <span data-ttu-id="b8ff4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ff4-119">-DefaultProfile</span></span>
<span data-ttu-id="b8ff4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8ff4-121">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="b8ff4-121">-ManagedInstanceName</span></span>
<span data-ttu-id="b8ff4-122">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-122">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases: InstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ff4-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8ff4-123">-Name</span></span>
<span data-ttu-id="b8ff4-124">Namnet på åtgärden.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-124">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: OperationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ff4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8ff4-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8ff4-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, ListByManagedInstanceParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ff4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8ff4-127">-ResourceId</span></span>
<span data-ttu-id="b8ff4-128">Resurs-ID för hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-128">The managed instance operation resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByManagedInstanceOperationResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ff4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ff4-129">CommonParameters</span></span>
<span data-ttu-id="b8ff4-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ff4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ff4-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8ff4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ff4-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8ff4-132">INPUTS</span></span>

### <span data-ttu-id="b8ff4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b8ff4-133">System.String</span></span>

## <span data-ttu-id="b8ff4-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8ff4-134">OUTPUTS</span></span>

### <span data-ttu-id="b8ff4-135">Microsoft. Azure. commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="b8ff4-135">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="b8ff4-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8ff4-136">NOTES</span></span>

## <span data-ttu-id="b8ff4-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8ff4-137">RELATED LINKS</span></span>