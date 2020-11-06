---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 6b787e3347c20e011193d0b3968e036d53f62226
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579948"
---
# <span data-ttu-id="bc418-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="bc418-101">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="bc418-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc418-102">SYNOPSIS</span></span>
<span data-ttu-id="bc418-103">Hämtar data masknings principen för en databas.</span><span class="sxs-lookup"><span data-stu-id="bc418-103">Gets the data masking policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc418-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc418-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc418-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc418-105">DESCRIPTION</span></span>
<span data-ttu-id="bc418-106">Cmdleten **Get-AzureRmSqlDatabaseDataMaskingPolicy** hämtar data masknings principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="bc418-106">The **Get-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="bc418-107">Använd den här cmdleten genom att använda parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="bc418-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="bc418-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="bc418-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="bc418-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc418-109">EXAMPLES</span></span>

### <span data-ttu-id="bc418-110">Exempel 1: Hämta data masknings principen för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="bc418-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="bc418-111">Det här kommandot hämtar principen data maskering från databas Database01 i resurs grupp ResourceGroup01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="bc418-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="bc418-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc418-112">PARAMETERS</span></span>

### <span data-ttu-id="bc418-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bc418-113">-DatabaseName</span></span>
<span data-ttu-id="bc418-114">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="bc418-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="bc418-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc418-115">-DefaultProfile</span></span>
<span data-ttu-id="bc418-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bc418-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc418-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc418-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc418-118">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="bc418-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="bc418-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bc418-119">-ServerName</span></span>
<span data-ttu-id="bc418-120">Anger namnet på den server där databasen finns.</span><span class="sxs-lookup"><span data-stu-id="bc418-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="bc418-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bc418-121">-Confirm</span></span>
<span data-ttu-id="bc418-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bc418-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc418-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc418-123">-WhatIf</span></span>
<span data-ttu-id="bc418-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bc418-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc418-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bc418-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc418-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc418-126">CommonParameters</span></span>
<span data-ttu-id="bc418-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc418-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc418-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc418-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc418-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc418-129">INPUTS</span></span>

### <span data-ttu-id="bc418-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bc418-130">System.String</span></span>

## <span data-ttu-id="bc418-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc418-131">OUTPUTS</span></span>

### <span data-ttu-id="bc418-132">Microsoft. Azure. commands. SQL. DataMasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="bc418-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="bc418-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc418-133">NOTES</span></span>

## <span data-ttu-id="bc418-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc418-134">RELATED LINKS</span></span>

[<span data-ttu-id="bc418-135">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bc418-135">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="bc418-136">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bc418-136">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="bc418-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bc418-137">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="bc418-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="bc418-138">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="bc418-139">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="bc418-139">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


