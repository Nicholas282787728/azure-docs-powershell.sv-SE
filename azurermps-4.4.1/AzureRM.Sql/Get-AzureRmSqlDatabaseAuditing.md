---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 4203609a97a9fc476292fca4020976539eb5d2b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585288"
---
# <span data-ttu-id="29ead-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="29ead-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="29ead-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29ead-102">SYNOPSIS</span></span>
<span data-ttu-id="29ead-103">Hämtar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="29ead-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29ead-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29ead-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29ead-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29ead-105">DESCRIPTION</span></span>
<span data-ttu-id="29ead-106">Cmdleten **Get-AzureRmSqlDatabaseAuditing** hämtar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="29ead-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="29ead-107">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="29ead-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="29ead-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29ead-108">EXAMPLES</span></span>

### <span data-ttu-id="29ead-109">Exempel 1: Hämta gransknings inställningar för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="29ead-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName           : database01
AuditAction            : {}
AuditActionGroup       : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                          BATCH_COMPLETED_GROUP, ...}
ResourceGroupName      : resourcegroup01
ServerName             : server01
AuditState             : Enabled
StorageAccountName     : mystorage
StorageKeyType         : Primary
RetentionInDays        : 0
```

## <span data-ttu-id="29ead-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29ead-110">PARAMETERS</span></span>

### <span data-ttu-id="29ead-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29ead-111">-DatabaseName</span></span>
<span data-ttu-id="29ead-112">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="29ead-112">SQL Database name.</span></span>

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

### <span data-ttu-id="29ead-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ead-113">-ResourceGroupName</span></span>
<span data-ttu-id="29ead-114">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="29ead-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="29ead-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29ead-115">-ServerName</span></span>
<span data-ttu-id="29ead-116">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="29ead-116">SQL Database server name.</span></span>

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

### <span data-ttu-id="29ead-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29ead-117">-Confirm</span></span>
<span data-ttu-id="29ead-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29ead-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29ead-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29ead-119">-WhatIf</span></span>
<span data-ttu-id="29ead-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29ead-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29ead-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29ead-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29ead-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ead-122">-DefaultProfile</span></span>
<span data-ttu-id="29ead-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29ead-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29ead-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ead-124">CommonParameters</span></span>
<span data-ttu-id="29ead-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29ead-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ead-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29ead-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ead-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29ead-127">INPUTS</span></span>

## <span data-ttu-id="29ead-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29ead-128">OUTPUTS</span></span>

### <span data-ttu-id="29ead-129">Microsoft. Azure. commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="29ead-129">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="29ead-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29ead-130">NOTES</span></span>

## <span data-ttu-id="29ead-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29ead-131">RELATED LINKS</span></span>

