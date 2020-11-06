---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 40674DC7-E35F-4C9F-8CE0-D1C6F524C9FB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: 1b4f72a5d57884975d6beb0d4676a0cbe5863681
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579935"
---
# <span data-ttu-id="0b549-101">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0b549-101">Get-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="0b549-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b549-102">SYNOPSIS</span></span>
<span data-ttu-id="0b549-103">Hämtar gransknings principen för en SQL-Server.</span><span class="sxs-lookup"><span data-stu-id="0b549-103">Gets the auditing policy of a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b549-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b549-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditingPolicy -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b549-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b549-105">DESCRIPTION</span></span>
<span data-ttu-id="0b549-106">Cmdleten **Get-AzureRmSqlServerAuditingPolicy** hämtar gransknings principen för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0b549-106">The **Get-AzureRmSqlServerAuditingPolicy** cmdlet gets the auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="0b549-107">Ange parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="0b549-107">Specify the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="0b549-108">Denna cmdlet returnerar en princip som används av de Azure SQL-databaser som båda är definierade i den angivna Azure SQL-servern och använder dess gransknings princip.</span><span class="sxs-lookup"><span data-stu-id="0b549-108">This cmdlet returns a policy that is used by the Azure SQL databases that are both defined in the specified Azure SQL server and use its auditing policy.</span></span>

## <span data-ttu-id="0b549-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b549-109">EXAMPLES</span></span>

### <span data-ttu-id="0b549-110">Exempel 1: Hämta gransknings princip för en Azure SQL Server med tabell granskning definierad</span><span class="sxs-lookup"><span data-stu-id="0b549-110">Example 1: Get the auditing policy of an Azure SQL server with Table auditing defined on it</span></span>
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

### <span data-ttu-id="0b549-111">Exempel 2: få gransknings policyn för en Azure SQL Server med BLOB-granskning definierad</span><span class="sxs-lookup"><span data-stu-id="0b549-111">Example 2: Get the auditing policy of an Azure SQL server with Blob auditing defined on it</span></span>
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

## <span data-ttu-id="0b549-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b549-112">PARAMETERS</span></span>

### <span data-ttu-id="0b549-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b549-113">-DefaultProfile</span></span>
<span data-ttu-id="0b549-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0b549-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b549-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b549-115">-ResourceGroupName</span></span>
<span data-ttu-id="0b549-116">Anger namnet på den resurs grupp som Azure SQL-servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="0b549-116">Specifies the name of the resource group to which the Azure SQL server is assigned.</span></span>

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

### <span data-ttu-id="0b549-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b549-117">-ServerName</span></span>
<span data-ttu-id="0b549-118">Anger namnet på den Azure SQL Server som den här cmdleten hämtar gransknings princip för.</span><span class="sxs-lookup"><span data-stu-id="0b549-118">Specifies the name of the Azure SQL server for which this cmdlet gets the auditing policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b549-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b549-119">-Confirm</span></span>
<span data-ttu-id="0b549-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b549-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b549-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b549-121">-WhatIf</span></span>
<span data-ttu-id="0b549-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b549-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b549-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b549-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b549-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b549-124">CommonParameters</span></span>
<span data-ttu-id="0b549-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b549-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b549-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b549-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b549-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b549-127">INPUTS</span></span>

### <span data-ttu-id="0b549-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0b549-128">System.String</span></span>

## <span data-ttu-id="0b549-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b549-129">OUTPUTS</span></span>

### <span data-ttu-id="0b549-130">Microsoft. Azure. commands. SQL. granskning. Model. AuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="0b549-130">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditingPolicyModel</span></span>

## <span data-ttu-id="0b549-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b549-131">NOTES</span></span>

## <span data-ttu-id="0b549-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b549-132">RELATED LINKS</span></span>

[<span data-ttu-id="0b549-133">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0b549-133">Set-AzureRmSqlServerAuditingPolicy</span></span>](./Set-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="0b549-134">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="0b549-134">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="0b549-135">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="0b549-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


