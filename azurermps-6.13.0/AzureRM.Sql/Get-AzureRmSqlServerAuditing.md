---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerAuditing.md
ms.openlocfilehash: bb26a4c237c056e5a86b47a8e7efa7458ab94487
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579932"
---
# <span data-ttu-id="cbd7c-101">Get-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="cbd7c-101">Get-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="cbd7c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cbd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd7c-103">Hämtar gransknings inställningarna för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-103">Gets the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbd7c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cbd7c-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerAuditing [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbd7c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cbd7c-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd7c-106">Cmdleten **Get-AzureRmSqlServerAuditing** hämtar BLOB-gransknings principen för en Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-106">The **Get-AzureRmSqlServerAuditing** cmdlet gets the blob auditing policy of an Azure SQL server.</span></span>
<span data-ttu-id="cbd7c-107">Ange parametrarna *ResourceGroupName* och *servername* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the database.</span></span>
<span data-ttu-id="cbd7c-108">Denna cmdlet returnerar en princip som används av de Azure SQL-databaser som har definierats i den angivna Azure SQL-servern.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-108">This cmdlet returns a policy that is used by the Azure SQL databases that are defined in the specified Azure SQL server.</span></span>

## <span data-ttu-id="cbd7c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cbd7c-109">EXAMPLES</span></span>

### <span data-ttu-id="cbd7c-110">Exempel 1: Hämta gransknings inställningar för en Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cbd7c-110">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzureRmSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

## <span data-ttu-id="cbd7c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cbd7c-111">PARAMETERS</span></span>

### <span data-ttu-id="cbd7c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd7c-112">-DefaultProfile</span></span>
<span data-ttu-id="cbd7c-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cbd7c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbd7c-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd7c-114">-ResourceGroupName</span></span>
<span data-ttu-id="cbd7c-115">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-115">The name of the resource group.</span></span>

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

### <span data-ttu-id="cbd7c-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cbd7c-116">-ServerName</span></span>
<span data-ttu-id="cbd7c-117">SQL Server-namn.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-117">SQL server name.</span></span>

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

### <span data-ttu-id="cbd7c-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cbd7c-118">-Confirm</span></span>
<span data-ttu-id="cbd7c-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbd7c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbd7c-120">-WhatIf</span></span>
<span data-ttu-id="cbd7c-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cbd7c-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbd7c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd7c-123">CommonParameters</span></span>
<span data-ttu-id="cbd7c-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd7c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd7c-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd7c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd7c-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cbd7c-126">INPUTS</span></span>

## <span data-ttu-id="cbd7c-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cbd7c-127">OUTPUTS</span></span>

### <span data-ttu-id="cbd7c-128">Microsoft. Azure. commands. SQL. granskning. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="cbd7c-128">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="cbd7c-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cbd7c-129">NOTES</span></span>

## <span data-ttu-id="cbd7c-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cbd7c-130">RELATED LINKS</span></span>
