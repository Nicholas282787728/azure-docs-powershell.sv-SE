---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: a12c9846b9e52d3c5e19c74b5a0f755acb27daf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575480"
---
# <span data-ttu-id="16317-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="16317-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="16317-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="16317-102">SYNOPSIS</span></span>
<span data-ttu-id="16317-103">Hämtar gransknings principen för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="16317-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16317-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="16317-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16317-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="16317-105">DESCRIPTION</span></span>
<span data-ttu-id="16317-106">Cmdleten **Get-AzureRmSqlServerAuditingPolicy** hämtar gransknings principen för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="16317-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="16317-107">Ange parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="16317-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="16317-108">Denna cmdlet returnerar en princip som används av de Azure SQL-databaser som båda är definierade i den angivna Azure SQL-servern och använder dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="16317-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="16317-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="16317-109">EXAMPLES</span></span>

### <span data-ttu-id="16317-110">Exempel 1: Hämta gransknings princip för en Azure SQL Server med tabell granskning definierad</span><span class="sxs-lookup"><span data-stu-id="16317-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="16317-111">Exempel 2: få gransknings policyn för en Azure SQL Server med BLOB-granskning definierad</span><span class="sxs-lookup"><span data-stu-id="16317-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditingPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

## <span data-ttu-id="16317-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="16317-112">PARAMETERS</span></span>

### <span data-ttu-id="16317-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16317-113">-DefaultProfile</span></span>
<span data-ttu-id="16317-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="16317-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16317-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16317-115">-ResourceGroupName</span></span>
<span data-ttu-id="16317-116">Anger namnet på den resurs grupp som Azure SQL-servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="16317-116">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="16317-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="16317-117">-ServerName</span></span>
<span data-ttu-id="16317-118">Anger namnet på den Azure SQL Server som den här cmdleten hämtar gransknings princip för.</span><span class="sxs-lookup"><span data-stu-id="16317-118">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

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

### <span data-ttu-id="16317-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="16317-119">-Confirm</span></span>
<span data-ttu-id="16317-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="16317-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16317-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16317-121">-WhatIf</span></span>
<span data-ttu-id="16317-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="16317-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16317-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="16317-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16317-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16317-124">CommonParameters</span></span>
<span data-ttu-id="16317-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16317-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16317-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16317-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16317-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="16317-127">INPUTS</span></span>

### <span data-ttu-id="16317-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="16317-128">None</span></span>
<span data-ttu-id="16317-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="16317-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16317-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="16317-130">OUTPUTS</span></span>

### <span data-ttu-id="16317-131">Microsoft. Azure. commands. SQL. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="16317-131">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="16317-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="16317-132">NOTES</span></span>

## <span data-ttu-id="16317-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="16317-133">RELATED LINKS</span></span>

[<span data-ttu-id="16317-134">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="16317-134">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="16317-135">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="16317-135">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="16317-136">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="16317-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


