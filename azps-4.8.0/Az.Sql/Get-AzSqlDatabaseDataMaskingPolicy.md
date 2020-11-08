---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100804"
---
# <span data-ttu-id="66fe7-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="66fe7-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="66fe7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="66fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="66fe7-103">Hämtar data masknings principen för en databas.</span><span class="sxs-lookup"><span data-stu-id="66fe7-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="66fe7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="66fe7-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="66fe7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="66fe7-105">DESCRIPTION</span></span>
<span data-ttu-id="66fe7-106">Cmdleten **Get-AzSqlDatabaseDataMaskingPolicy** hämtar data masknings principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="66fe7-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="66fe7-107">Använd den här cmdleten genom att använda parametrarna *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="66fe7-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="66fe7-108">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="66fe7-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="66fe7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="66fe7-109">EXAMPLES</span></span>

### <span data-ttu-id="66fe7-110">Exempel 1: Hämta data masknings principen för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="66fe7-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="66fe7-111">Det här kommandot hämtar principen data maskering från databas Database01 i resurs grupp ResourceGroup01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="66fe7-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="66fe7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="66fe7-112">PARAMETERS</span></span>

### <span data-ttu-id="66fe7-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="66fe7-113">-DatabaseName</span></span>
<span data-ttu-id="66fe7-114">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="66fe7-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="66fe7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66fe7-115">-DefaultProfile</span></span>
<span data-ttu-id="66fe7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="66fe7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66fe7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66fe7-117">-ResourceGroupName</span></span>
<span data-ttu-id="66fe7-118">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="66fe7-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="66fe7-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66fe7-119">-ServerName</span></span>
<span data-ttu-id="66fe7-120">Anger namnet på den server där databasen finns.</span><span class="sxs-lookup"><span data-stu-id="66fe7-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="66fe7-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="66fe7-121">-Confirm</span></span>
<span data-ttu-id="66fe7-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="66fe7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66fe7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66fe7-123">-WhatIf</span></span>
<span data-ttu-id="66fe7-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="66fe7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66fe7-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="66fe7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66fe7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66fe7-126">CommonParameters</span></span>
<span data-ttu-id="66fe7-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66fe7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66fe7-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66fe7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66fe7-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="66fe7-129">INPUTS</span></span>

### <span data-ttu-id="66fe7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="66fe7-130">System.String</span></span>

## <span data-ttu-id="66fe7-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="66fe7-131">OUTPUTS</span></span>

### <span data-ttu-id="66fe7-132">Microsoft. Azure. commands. SQL. DataMasking. Model. DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="66fe7-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="66fe7-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="66fe7-133">NOTES</span></span>

## <span data-ttu-id="66fe7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="66fe7-134">RELATED LINKS</span></span>

[<span data-ttu-id="66fe7-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="66fe7-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="66fe7-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="66fe7-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="66fe7-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="66fe7-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="66fe7-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="66fe7-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="66fe7-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="66fe7-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


