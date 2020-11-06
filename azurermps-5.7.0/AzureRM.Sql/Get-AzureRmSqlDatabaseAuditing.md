---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 9058863da0af6addd243f5e7ec544a8dad7b3b03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573220"
---
# <span data-ttu-id="10c2b-101">Get-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="10c2b-101">Get-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="10c2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="10c2b-103">Hämtar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="10c2b-103">Gets the auditing settings of an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10c2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10c2b-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseAuditing [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10c2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10c2b-105">DESCRIPTION</span></span>
<span data-ttu-id="10c2b-106">Cmdleten **Get-AzureRmSqlDatabaseAuditing** hämtar gransknings inställningarna för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="10c2b-106">The **Get-AzureRmSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="10c2b-107">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="10c2b-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="10c2b-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10c2b-108">EXAMPLES</span></span>

### <span data-ttu-id="10c2b-109">Exempel 1: Hämta gransknings inställningar för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="10c2b-109">Example 1: Get the auditing settings of an Azure SQL database</span></span>
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

## <span data-ttu-id="10c2b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10c2b-110">PARAMETERS</span></span>

### <span data-ttu-id="10c2b-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="10c2b-111">-DatabaseName</span></span>
<span data-ttu-id="10c2b-112">Namn på SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="10c2b-112">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10c2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c2b-113">-DefaultProfile</span></span>
<span data-ttu-id="10c2b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="10c2b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10c2b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c2b-115">-ResourceGroupName</span></span>
<span data-ttu-id="10c2b-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="10c2b-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="10c2b-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10c2b-117">-ServerName</span></span>
<span data-ttu-id="10c2b-118">Server namn för SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="10c2b-118">SQL Database server name.</span></span>

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

### <span data-ttu-id="10c2b-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10c2b-119">-Confirm</span></span>
<span data-ttu-id="10c2b-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10c2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c2b-121">-WhatIf</span></span>
<span data-ttu-id="10c2b-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10c2b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10c2b-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10c2b-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c2b-124">CommonParameters</span></span>
<span data-ttu-id="10c2b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c2b-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10c2b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c2b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10c2b-127">INPUTS</span></span>

### <span data-ttu-id="10c2b-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="10c2b-128">None</span></span>
<span data-ttu-id="10c2b-129">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="10c2b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10c2b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10c2b-130">OUTPUTS</span></span>

### <span data-ttu-id="10c2b-131">Microsoft. Azure. commands. SQL. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="10c2b-131">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="10c2b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10c2b-132">NOTES</span></span>

## <span data-ttu-id="10c2b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10c2b-133">RELATED LINKS</span></span>
