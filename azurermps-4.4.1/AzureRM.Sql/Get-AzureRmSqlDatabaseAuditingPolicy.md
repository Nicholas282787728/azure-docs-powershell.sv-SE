---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: a6fe2e171338885af2367d6fec1cc3a97002b321
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585287"
---
# <span data-ttu-id="1efcc-101">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="1efcc-101">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="1efcc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1efcc-102">SYNOPSIS</span></span>
<span data-ttu-id="1efcc-103">Hämtar gransknings principen för en databas.</span><span class="sxs-lookup"><span data-stu-id="1efcc-103">Gets the auditing policy of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1efcc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1efcc-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1efcc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1efcc-105">DESCRIPTION</span></span>
<span data-ttu-id="1efcc-106">Cmdleten **Get-AzureRmSqlDatabaseAuditingPolicy** hämtar gransknings principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="1efcc-106">The **Get-AzureRmSqlDatabaseAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL Database.</span></span>
<span data-ttu-id="1efcc-107">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="1efcc-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="1efcc-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1efcc-108">EXAMPLES</span></span>

### <span data-ttu-id="1efcc-109">Exempel 1: få gransknings policyn för en Azure SQL-databas med tabell granskning definierad</span><span class="sxs-lookup"><span data-stu-id="1efcc-109">Example 1: Get the auditing policy of an Azure SQL database with Table auditing defined on it</span></span>
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

### <span data-ttu-id="1efcc-110">Exempel 2: Hämta en gransknings princip för en Azure SQL-databas med BLOB audit definierad</span><span class="sxs-lookup"><span data-stu-id="1efcc-110">Example 2: Get the auditing policy of an Azure SQL database with Blob auditing defined on it</span></span>
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

## <span data-ttu-id="1efcc-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1efcc-111">PARAMETERS</span></span>

### <span data-ttu-id="1efcc-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1efcc-112">-DatabaseName</span></span>
<span data-ttu-id="1efcc-113">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="1efcc-113">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1efcc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1efcc-114">-ResourceGroupName</span></span>
<span data-ttu-id="1efcc-115">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="1efcc-115">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1efcc-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1efcc-116">-ServerName</span></span>
<span data-ttu-id="1efcc-117">Anger namnet på den server där databasen finns.</span><span class="sxs-lookup"><span data-stu-id="1efcc-117">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="1efcc-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1efcc-118">-Confirm</span></span>
<span data-ttu-id="1efcc-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1efcc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1efcc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1efcc-120">-WhatIf</span></span>
<span data-ttu-id="1efcc-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1efcc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1efcc-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1efcc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1efcc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1efcc-123">-DefaultProfile</span></span>
<span data-ttu-id="1efcc-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1efcc-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1efcc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1efcc-125">CommonParameters</span></span>
<span data-ttu-id="1efcc-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1efcc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1efcc-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1efcc-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1efcc-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1efcc-128">INPUTS</span></span>

## <span data-ttu-id="1efcc-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1efcc-129">OUTPUTS</span></span>

### <span data-ttu-id="1efcc-130">Microsoft. Azure. commands. SQL. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="1efcc-130">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="1efcc-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1efcc-131">NOTES</span></span>

## <span data-ttu-id="1efcc-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1efcc-132">RELATED LINKS</span></span>

[<span data-ttu-id="1efcc-133">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="1efcc-133">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="1efcc-134">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="1efcc-134">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Set-AzureRmSqlDatabaseAuditingPolicy.md)



