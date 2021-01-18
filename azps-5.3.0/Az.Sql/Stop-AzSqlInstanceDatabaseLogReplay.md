---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Stop-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 2a7c74c4c8fef61e01ccbbb512ff428b9e885f06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522759"
---
# <span data-ttu-id="318ea-101">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="318ea-101">Stop-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="318ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="318ea-102">SYNOPSIS</span></span>
<span data-ttu-id="318ea-103">Avbryter loggen genom att släppa databasen.</span><span class="sxs-lookup"><span data-stu-id="318ea-103">Cancels the Log Replay service by dropping the database.</span></span>

## <span data-ttu-id="318ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="318ea-104">SYNTAX</span></span>

### <span data-ttu-id="318ea-105">LogReplayInstanceDatabaseFromInputParameters (standard)</span><span class="sxs-lookup"><span data-stu-id="318ea-105">LogReplayInstanceDatabaseFromInputParameters (Default)</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="318ea-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="318ea-106">LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Stop-AzSqlInstanceDatabaseLogReplay [-Force] [-PassThru] [-InputObject] <AzureSqlManagedDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="318ea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="318ea-107">DESCRIPTION</span></span>
<span data-ttu-id="318ea-108">Cmdleten **Stop-AzSqlInstanceDatabaseLogReplay** avslutar databasen och avslutar sedan logg tjänsten.</span><span class="sxs-lookup"><span data-stu-id="318ea-108">The **Stop-AzSqlInstanceDatabaseLogReplay** cmdlet drops the database and thus cancel Log Replay service.</span></span>

## <span data-ttu-id="318ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="318ea-109">EXAMPLES</span></span>

### <span data-ttu-id="318ea-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="318ea-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="318ea-111">Det här kommandot avslutar loggnings tjänsten för den angivna databasen.</span><span class="sxs-lookup"><span data-stu-id="318ea-111">This command will cancel log replay service on the given database.</span></span>

## <span data-ttu-id="318ea-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="318ea-112">PARAMETERS</span></span>

### <span data-ttu-id="318ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="318ea-113">-DefaultProfile</span></span>
<span data-ttu-id="318ea-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="318ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="318ea-115">-Force</span><span class="sxs-lookup"><span data-stu-id="318ea-115">-Force</span></span>
<span data-ttu-id="318ea-116">Hoppa över bekräftelse meddelande för att utföra åtgärden</span><span class="sxs-lookup"><span data-stu-id="318ea-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="318ea-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="318ea-117">-InputObject</span></span>
<span data-ttu-id="318ea-118">Instans databas objekt.</span><span class="sxs-lookup"><span data-stu-id="318ea-118">The instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: LogReplayInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="318ea-119">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="318ea-119">-InstanceName</span></span>
<span data-ttu-id="318ea-120">Namnet på instansen.</span><span class="sxs-lookup"><span data-stu-id="318ea-120">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318ea-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="318ea-121">-Name</span></span>
<span data-ttu-id="318ea-122">Namnet på instans databasen.</span><span class="sxs-lookup"><span data-stu-id="318ea-122">The name of the instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318ea-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="318ea-123">-PassThru</span></span>
<span data-ttu-id="318ea-124">Definierar om synkroniseringsresursen ska returneras.</span><span class="sxs-lookup"><span data-stu-id="318ea-124">Defines Whether return the sync group.</span></span>

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

### <span data-ttu-id="318ea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="318ea-125">-ResourceGroupName</span></span>
<span data-ttu-id="318ea-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="318ea-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: LogReplayInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="318ea-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="318ea-127">-Confirm</span></span>
<span data-ttu-id="318ea-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="318ea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="318ea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="318ea-129">-WhatIf</span></span>
<span data-ttu-id="318ea-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="318ea-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="318ea-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="318ea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="318ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="318ea-132">CommonParameters</span></span>
<span data-ttu-id="318ea-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="318ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="318ea-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="318ea-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="318ea-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="318ea-135">INPUTS</span></span>

### <span data-ttu-id="318ea-136">System. String</span><span class="sxs-lookup"><span data-stu-id="318ea-136">System.String</span></span>

### <span data-ttu-id="318ea-137">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="318ea-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="318ea-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="318ea-138">OUTPUTS</span></span>

### <span data-ttu-id="318ea-139">Microsoft. Azure. commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="318ea-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="318ea-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="318ea-140">NOTES</span></span>

## <span data-ttu-id="318ea-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="318ea-141">RELATED LINKS</span></span>
