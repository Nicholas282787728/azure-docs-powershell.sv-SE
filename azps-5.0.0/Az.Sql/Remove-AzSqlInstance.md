---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstance.md
ms.openlocfilehash: e361dc9a224649b7b1af38594145f14e24091d7a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273023"
---
# <span data-ttu-id="058d0-101">Remove-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="058d0-101">Remove-AzSqlInstance</span></span>

## <span data-ttu-id="058d0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="058d0-102">SYNOPSIS</span></span>
<span data-ttu-id="058d0-103">Tar bort en Azure SQL-hanterad databas instans.</span><span class="sxs-lookup"><span data-stu-id="058d0-103">Removes an Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="058d0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="058d0-104">SYNTAX</span></span>

### <span data-ttu-id="058d0-105">RemoveInstanceFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="058d0-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058d0-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="058d0-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="058d0-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="058d0-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="058d0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="058d0-108">DESCRIPTION</span></span>
<span data-ttu-id="058d0-109">Cmdleten **Remove-AzSqlInstance** tar bort en hanterad instans av en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="058d0-109">The **Remove-AzSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="058d0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="058d0-110">EXAMPLES</span></span>

### <span data-ttu-id="058d0-111">Exempel 1: ta bort instans</span><span class="sxs-lookup"><span data-stu-id="058d0-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="058d0-112">Det här kommandot tar bort förekomsten med namnet managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="058d0-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="058d0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="058d0-113">PARAMETERS</span></span>

### <span data-ttu-id="058d0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058d0-114">-DefaultProfile</span></span>
<span data-ttu-id="058d0-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="058d0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="058d0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="058d0-116">-Force</span></span>
<span data-ttu-id="058d0-117">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="058d0-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="058d0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="058d0-118">-InputObject</span></span>
<span data-ttu-id="058d0-119">AzureSqlManagedInstanceModel-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="058d0-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="058d0-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="058d0-120">-Name</span></span>
<span data-ttu-id="058d0-121">SQL-instansnamn.</span><span class="sxs-lookup"><span data-stu-id="058d0-121">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="058d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="058d0-123">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="058d0-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="058d0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="058d0-124">-ResourceId</span></span>
<span data-ttu-id="058d0-125">Resurs-ID för instans objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="058d0-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="058d0-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="058d0-126">-Confirm</span></span>
<span data-ttu-id="058d0-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="058d0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="058d0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="058d0-128">-WhatIf</span></span>
<span data-ttu-id="058d0-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="058d0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="058d0-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="058d0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="058d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058d0-131">CommonParameters</span></span>
<span data-ttu-id="058d0-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="058d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058d0-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="058d0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058d0-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="058d0-134">INPUTS</span></span>

### <span data-ttu-id="058d0-135">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="058d0-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="058d0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="058d0-136">System.String</span></span>

## <span data-ttu-id="058d0-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="058d0-137">OUTPUTS</span></span>

### <span data-ttu-id="058d0-138">Microsoft. Azure. commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="058d0-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="058d0-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="058d0-139">NOTES</span></span>

## <span data-ttu-id="058d0-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="058d0-140">RELATED LINKS</span></span>
