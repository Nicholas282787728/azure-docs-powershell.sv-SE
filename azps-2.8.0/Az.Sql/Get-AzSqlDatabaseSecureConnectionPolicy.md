---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: d160e6cf954240495a9f9b3969d87dab6d880e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920393"
---
# <span data-ttu-id="cd690-101">Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd690-101">Get-AzSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="cd690-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd690-102">SYNOPSIS</span></span>
<span data-ttu-id="cd690-103">Hämtar den säkra anslutnings principen för en databas.</span><span class="sxs-lookup"><span data-stu-id="cd690-103">Gets the secure connection policy for a database.</span></span> <span data-ttu-id="cd690-104">Säker anslutning är inaktuellt och det här kommandot tas bort i framtida versioner.</span><span class="sxs-lookup"><span data-stu-id="cd690-104">Secure connection is deprecated and this command will be removed in a future release.</span></span> <span data-ttu-id="cd690-105">Använd SQL-databasens blad i Azure-portalen för att Visa anslutnings strängarna</span><span class="sxs-lookup"><span data-stu-id="cd690-105">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

## <span data-ttu-id="cd690-106">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd690-106">SYNTAX</span></span>

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd690-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd690-107">DESCRIPTION</span></span>
<span data-ttu-id="cd690-108">Cmdleten **Get-AzSqlDatabaseSecureConnectionPolicy** hämtar den krypterade kanal principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="cd690-108">The **Get-AzSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="cd690-109">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="cd690-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="cd690-110">När denna cmdlet körs returneras ett objekt som beskriver den aktuella krypterade kanal principen och även databas identifierarna.</span><span class="sxs-lookup"><span data-stu-id="cd690-110">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="cd690-111">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="cd690-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="cd690-112">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="cd690-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cd690-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd690-113">EXAMPLES</span></span>

### <span data-ttu-id="cd690-114">Exempel 1: hämta den krypterade kanal principen för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="cd690-114">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="cd690-115">Det här kommandot hämtar den krypterade kanal principen för en Azure SQL-databas som heter database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="cd690-115">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="cd690-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd690-116">PARAMETERS</span></span>

### <span data-ttu-id="cd690-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd690-117">-DatabaseName</span></span>
<span data-ttu-id="cd690-118">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="cd690-118">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="cd690-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd690-119">-DefaultProfile</span></span>
<span data-ttu-id="cd690-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cd690-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd690-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd690-121">-ResourceGroupName</span></span>
<span data-ttu-id="cd690-122">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="cd690-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="cd690-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cd690-123">-ServerName</span></span>
<span data-ttu-id="cd690-124">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="cd690-124">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="cd690-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd690-125">-Confirm</span></span>
<span data-ttu-id="cd690-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd690-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd690-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd690-127">-WhatIf</span></span>
<span data-ttu-id="cd690-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd690-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd690-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd690-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd690-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd690-130">CommonParameters</span></span>
<span data-ttu-id="cd690-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd690-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd690-132">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd690-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd690-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd690-133">INPUTS</span></span>

### <span data-ttu-id="cd690-134">System. String</span><span class="sxs-lookup"><span data-stu-id="cd690-134">System.String</span></span>

## <span data-ttu-id="cd690-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd690-135">OUTPUTS</span></span>

### <span data-ttu-id="cd690-136">Microsoft. Azure. commands. SQL. SecureConnection. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cd690-136">Microsoft.Azure.Commands.Sql.SecureConnection.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="cd690-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd690-137">NOTES</span></span>

## <span data-ttu-id="cd690-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd690-138">RELATED LINKS</span></span>
