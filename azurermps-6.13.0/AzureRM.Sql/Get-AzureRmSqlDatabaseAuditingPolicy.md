---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a37bf2dd4e69352ff33a1f8c886750fec67e52f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579951"
---
# <span data-ttu-id="761dd-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="761dd-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="761dd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="761dd-102">SYNOPSIS</span></span>
<span data-ttu-id="761dd-103">Hämtar gransknings principen för en databas.</span><span class="sxs-lookup"><span data-stu-id="761dd-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="761dd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="761dd-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="761dd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="761dd-105">DESCRIPTION</span></span>
<span data-ttu-id="761dd-106">Cmdleten **Get-AzureRmSqlDatabaseAuditingPolicy** hämtar gransknings principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="761dd-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="761dd-107">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="761dd-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="761dd-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="761dd-108">EXAMPLES</span></span>

### <span data-ttu-id="761dd-109">Exempel 1: få gransknings policyn för en Azure SQL-databas med tabell granskning definierad</span><span class="sxs-lookup"><span data-stu-id="761dd-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
UseServerDefault       : Disabled
EventType              : {PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure...} 
TableIdentifier        : MyAuditTableName
FullAuditLogsTableName : SQLDBAuditLogsMyAuditTableName
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Table
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

### <span data-ttu-id="761dd-110">Exempel 2: Hämta en gransknings princip för en Azure SQL-databas med BLOB audit definierad</span><span class="sxs-lookup"><span data-stu-id="761dd-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...} 
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditType              : Blob
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="761dd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="761dd-111">PARAMETERS</span></span>

### <span data-ttu-id="761dd-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="761dd-112">-DatabaseName</span></span>
<span data-ttu-id="761dd-113">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="761dd-113">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="761dd-114">-DefaultProfile</span></span>
<span data-ttu-id="761dd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="761dd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="761dd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="761dd-116">-ResourceGroupName</span></span>
<span data-ttu-id="761dd-117">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="761dd-117">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761dd-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="761dd-118">-ServerName</span></span>
<span data-ttu-id="761dd-119">Anger namnet på den server där databasen finns.</span><span class="sxs-lookup"><span data-stu-id="761dd-119">Specifies the name of the server where the database is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761dd-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="761dd-120">-Confirm</span></span>
<span data-ttu-id="761dd-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="761dd-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="761dd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="761dd-122">-WhatIf</span></span>
<span data-ttu-id="761dd-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="761dd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="761dd-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="761dd-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="761dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="761dd-125">CommonParameters</span></span>
<span data-ttu-id="761dd-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="761dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="761dd-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="761dd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="761dd-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="761dd-128">INPUTS</span></span>

### <span data-ttu-id="761dd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="761dd-129">System.String</span></span>

## <span data-ttu-id="761dd-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="761dd-130">OUTPUTS</span></span>

### <span data-ttu-id="761dd-131">Microsoft. Azure. commands. SQL. granskning. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="761dd-131">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="761dd-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="761dd-132">NOTES</span></span>

## <span data-ttu-id="761dd-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="761dd-133">RELATED LINKS</span></span>

[<span data-ttu-id="761dd-134">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="761dd-134">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="761dd-135">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="761dd-135">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



