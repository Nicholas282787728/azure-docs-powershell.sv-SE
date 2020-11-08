---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlinstanceoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceOperation.md
ms.openlocfilehash: c57b704f54eacbd9b5cac808e69f9bbf289dc0cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100771"
---
# <span data-ttu-id="7e855-101">Stop-AzSqlInstanceOperation</span><span class="sxs-lookup"><span data-stu-id="7e855-101">Stop-AzSqlInstanceOperation</span></span>

## <span data-ttu-id="7e855-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7e855-102">SYNOPSIS</span></span>
<span data-ttu-id="7e855-103">Stoppar en SQL-hanterad instanss operationer.</span><span class="sxs-lookup"><span data-stu-id="7e855-103">Stops a SQL managed instance's operations.</span></span>

## <span data-ttu-id="7e855-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7e855-104">SYNTAX</span></span>

### <span data-ttu-id="7e855-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7e855-105">StopByNameAndManagedInstanceAndResourceGroupParameterSet (Default)</span></span>
```
Stop-AzSqlInstanceOperation [-Name] <String> [-ManagedInstanceName] <String> [-ResourceGroupName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e855-106">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e855-106">StopByResourceIdParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e855-107">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e855-107">StopByInputObjectParameterSet</span></span>
```
Stop-AzSqlInstanceOperation [-InputObject] <AzureSqlManagedInstanceOperationModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e855-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7e855-108">DESCRIPTION</span></span>
<span data-ttu-id="7e855-109">Stop-AzSqlInstanceOperation cmdlet stoppar åtgärden med det här namnet på en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="7e855-109">The Stop-AzSqlInstanceOperation cmdlet stops operation with provided operation name on a SQL managed instance.</span></span>

## <span data-ttu-id="7e855-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7e855-110">EXAMPLES</span></span>

### <span data-ttu-id="7e855-111">Exempel 1: få en särskild åtgärd</span><span class="sxs-lookup"><span data-stu-id="7e855-111">Example 1: Get a specific operation</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name d0f5bef5-e2b1-4ef8-bb42-2e54073874f9

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : d0f5bef5-e2b1-4ef8-bb42-2e54073874f9
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:49:53 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="7e855-112">Det här kommandot stoppar åtgärden med namnet ' d0f5bef5-e2b1-4ef8-bb42-2e54073874f9 ' på en SQL-hanterad instans.</span><span class="sxs-lookup"><span data-stu-id="7e855-112">This command stops operation with name 'd0f5bef5-e2b1-4ef8-bb42-2e54073874f9' on a SQL managed instance.</span></span>

### <span data-ttu-id="7e855-113">Exempel 2: använda resurs-ID för operation</span><span class="sxs-lookup"><span data-stu-id="7e855-113">Example 2: Using operation resource id</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name 4253bf58-34f1-4499-80c6-198d94c659f7
PS C:\> Get-AzSqlInstanceOperation -ResourceId $managedInstanceOperation.Id

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/4253bf58-34f1-4499-80c6-198d94c659f7
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : 4253bf58-34f1-4499-80c6-198d94c659f7
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:47:32 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="7e855-114">Det här kommandot stoppar åtgärden med resurs-ID $managedInstanceOperation. ID.</span><span class="sxs-lookup"><span data-stu-id="7e855-114">This command stops operation with resource id $managedInstanceOperation.Id.</span></span>

### <span data-ttu-id="7e855-115">Exempel 3: använda Operations-objekt</span><span class="sxs-lookup"><span data-stu-id="7e855-115">Example 3: Using operation object</span></span>
```powershell
PS C:\> $managedInstanceOperation = Get-AzSqlInstanceOperation -ResourceGroupName ps3753 -ManagedInstanceName ps3698 -Name b15a2b78-c42c-4e00-bf87-7ef4737552dc
PS C:\> Stop-AzSqlInstanceOperation -InputObject $managedInstanceOperation

Id                      : /subscriptions/a8c9a924-06c0-4bde-9788-e7b1370969e1/resourceGroups/ps3753/providers/Microsoft.Sql/managedInstances/ps3698/operations/b15a2b78-c42c-4e00-bf87-7ef4737552dc
ResourceGroupName       : ps3753
ManagedInstanceName     : ps3698
Name                    : b15a2b78-c42c-4e00-bf87-7ef4737552dc
Operation               : UpsertManagedServer
OperationFriendlyName   : UPDATE MANAGED SERVER
PercentComplete         : 0
StartTime               : 3/16/2020 12:44:57 PM
State                   : InProgress
ErrorCode               :
ErrorDescription        :
ErrorSeverity           :
IsUserError             :
EstimatedCompletionTime :
Description             :
IsCancellable           : True
```

<span data-ttu-id="7e855-116">Det här kommandot stoppar åtgärden med objekt $managedInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="7e855-116">This command stops operation with object $managedInstanceOperation.</span></span>

## <span data-ttu-id="7e855-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7e855-117">PARAMETERS</span></span>

### <span data-ttu-id="7e855-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e855-118">-DefaultProfile</span></span>
<span data-ttu-id="7e855-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7e855-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e855-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7e855-120">-Force</span></span>
<span data-ttu-id="7e855-121">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="7e855-121">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e855-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e855-122">-InputObject</span></span>
<span data-ttu-id="7e855-123">Åtgärden att annullera</span><span class="sxs-lookup"><span data-stu-id="7e855-123">The operation to cancel</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel
Parameter Sets: StopByInputObjectParameterSet
Aliases: SqlInstanceOperation

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e855-124">-ManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="7e855-124">-ManagedInstanceName</span></span>
<span data-ttu-id="7e855-125">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="7e855-125">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e855-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="7e855-126">-Name</span></span>
<span data-ttu-id="7e855-127">Namnet på åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7e855-127">The name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases: OperationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e855-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e855-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e855-129">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7e855-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameAndManagedInstanceAndResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e855-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e855-130">-ResourceId</span></span>
<span data-ttu-id="7e855-131">Resurs-ID för åtgärden åtgärd för att stoppa</span><span class="sxs-lookup"><span data-stu-id="7e855-131">The resource id of operation object to stop</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e855-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7e855-132">-Confirm</span></span>
<span data-ttu-id="7e855-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7e855-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e855-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e855-134">-WhatIf</span></span>
<span data-ttu-id="7e855-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7e855-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e855-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7e855-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e855-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e855-137">CommonParameters</span></span>
<span data-ttu-id="7e855-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e855-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e855-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e855-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e855-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7e855-140">INPUTS</span></span>

### <span data-ttu-id="7e855-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7e855-141">System.String</span></span>

### <span data-ttu-id="7e855-142">Microsoft. Azure. commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="7e855-142">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="7e855-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7e855-143">OUTPUTS</span></span>

### <span data-ttu-id="7e855-144">Microsoft. Azure. commands. SQL. ManagedInstanceOperation. Model. AzureSqlManagedInstanceOperationModel</span><span class="sxs-lookup"><span data-stu-id="7e855-144">Microsoft.Azure.Commands.Sql.ManagedInstanceOperation.Model.AzureSqlManagedInstanceOperationModel</span></span>

## <span data-ttu-id="7e855-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7e855-145">NOTES</span></span>

## <span data-ttu-id="7e855-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7e855-146">RELATED LINKS</span></span>
