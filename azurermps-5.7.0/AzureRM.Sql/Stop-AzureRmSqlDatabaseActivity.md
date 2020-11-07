---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: d0aa42b8b584ade698c3d03848a537350ac342d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756438"
---
# <span data-ttu-id="a6800-101">Stop-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="a6800-101">Stop-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="a6800-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6800-102">SYNOPSIS</span></span>
<span data-ttu-id="a6800-103">Avbryter den asynkrona uppdateringen av databasen.</span><span class="sxs-lookup"><span data-stu-id="a6800-103">Cancels the asynchronous updates operation on the database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6800-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6800-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6800-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6800-105">DESCRIPTION</span></span>
<span data-ttu-id="a6800-106">Cmdleten **Stop-AzureRmSqlDatabaseActivity** avbryter den asynkrona uppdateringen av databasen.</span><span class="sxs-lookup"><span data-stu-id="a6800-106">The **Stop-AzureRmSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="a6800-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6800-107">EXAMPLES</span></span>

### <span data-ttu-id="a6800-108">Exempel 1: Avbryt den asynkrona uppdateringen i databasen</span><span class="sxs-lookup"><span data-stu-id="a6800-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="a6800-109">Det här kommandot avbryter den asynkrona uppdateringen av databasen.</span><span class="sxs-lookup"><span data-stu-id="a6800-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="a6800-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6800-110">PARAMETERS</span></span>

### <span data-ttu-id="a6800-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a6800-111">-DatabaseName</span></span>
<span data-ttu-id="a6800-112">Anger namnet på den databas där denna cmdlet får status.</span><span class="sxs-lookup"><span data-stu-id="a6800-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6800-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6800-113">-DefaultProfile</span></span>
<span data-ttu-id="a6800-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a6800-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6800-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a6800-115">-ElasticPoolName</span></span>
<span data-ttu-id="a6800-116">Namnet på den elastiska Azure SQL-poolen.</span><span class="sxs-lookup"><span data-stu-id="a6800-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6800-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a6800-117">-OperationId</span></span>
<span data-ttu-id="a6800-118">Anger ID för den operation som denna cmdlet får.</span><span class="sxs-lookup"><span data-stu-id="a6800-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6800-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6800-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6800-120">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="a6800-120">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6800-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a6800-121">-ServerName</span></span>
<span data-ttu-id="a6800-122">Anger namnet på den Microsoft SQL Server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="a6800-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6800-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6800-123">-Confirm</span></span>
<span data-ttu-id="a6800-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6800-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6800-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6800-125">-WhatIf</span></span>
<span data-ttu-id="a6800-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6800-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6800-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6800-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6800-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6800-128">CommonParameters</span></span>
<span data-ttu-id="a6800-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6800-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6800-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6800-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6800-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6800-131">INPUTS</span></span>

### <span data-ttu-id="a6800-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="a6800-132">None</span></span>
<span data-ttu-id="a6800-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a6800-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6800-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6800-134">OUTPUTS</span></span>

### <span data-ttu-id="a6800-135">Microsoft. Azure. commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="a6800-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="a6800-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6800-136">NOTES</span></span>

## <span data-ttu-id="a6800-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6800-137">RELATED LINKS</span></span>
