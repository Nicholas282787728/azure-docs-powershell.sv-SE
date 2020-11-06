---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: 3b63aea46cbff930303f8f8e58a66923a6df46b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574979"
---
# <span data-ttu-id="c6aa4-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c6aa4-101">Get-AzureRmSqlDatabaseSecureConnectionPolicy</span></span>

## <span data-ttu-id="c6aa4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6aa4-102">SYNOPSIS</span></span>
<span data-ttu-id="c6aa4-103">Hämtar den säkra anslutnings principen för en databas.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-103">Gets the secure connection policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6aa4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6aa4-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6aa4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6aa4-105">DESCRIPTION</span></span>
<span data-ttu-id="c6aa4-106">Cmdleten **Get-AzureRmSqlDatabaseSecureConnectionPolicy** hämtar den krypterade kanal principen för en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-106">The **Get-AzureRmSqlDatabaseSecureConnectionPolicy** cmdlet gets the encrypted channel policy of an Azure SQL database.</span></span>
<span data-ttu-id="c6aa4-107">Använd cmdleten *ResourceGroupName* , *servername* och *databasename* för att identifiera databasen.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c6aa4-108">När denna cmdlet körs returneras ett objekt som beskriver den aktuella krypterade kanal principen och även databas identifierarna.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-108">After this cmdlet runs successfully, it returns an object that describes the current encrypted channel policy and also the database identifiers.</span></span>
<span data-ttu-id="c6aa4-109">Databas identifierare inkluderar, men är inte begränsade till, **ResourceGroupName** , **servername** och **databasename**.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-109">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="c6aa4-110">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c6aa4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6aa4-111">EXAMPLES</span></span>

### <span data-ttu-id="c6aa4-112">Exempel 1: hämta den krypterade kanal principen för en Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="c6aa4-112">Example 1: Get the encrypted channel policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

<span data-ttu-id="c6aa4-113">Det här kommandot hämtar den krypterade kanal principen för en Azure SQL-databas som heter database01 på Server Server01.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-113">This command gets the encrypted channel policy of an Azure SQL database named database01 located on server server01.</span></span>

## <span data-ttu-id="c6aa4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6aa4-114">PARAMETERS</span></span>

### <span data-ttu-id="c6aa4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c6aa4-115">-DatabaseName</span></span>
<span data-ttu-id="c6aa4-116">Anger namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-116">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="c6aa4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6aa4-117">-ResourceGroupName</span></span>
<span data-ttu-id="c6aa4-118">Anger namnet på den resurs grupp som databasen har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c6aa4-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6aa4-119">-ServerName</span></span>
<span data-ttu-id="c6aa4-120">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-120">Specifies the name of server that hosts the database.</span></span>

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

### <span data-ttu-id="c6aa4-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6aa4-121">-Confirm</span></span>
<span data-ttu-id="c6aa4-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6aa4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6aa4-123">-WhatIf</span></span>
<span data-ttu-id="c6aa4-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6aa4-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6aa4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6aa4-126">-DefaultProfile</span></span>
<span data-ttu-id="c6aa4-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6aa4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6aa4-128">CommonParameters</span></span>
<span data-ttu-id="c6aa4-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6aa4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6aa4-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6aa4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6aa4-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6aa4-131">INPUTS</span></span>

## <span data-ttu-id="c6aa4-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6aa4-132">OUTPUTS</span></span>

### <span data-ttu-id="c6aa4-133">Microsoft. Azure. commands. SQL. Security. Model. DatabaseSecureConnectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c6aa4-133">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseSecureConnectionPolicyModel</span></span>

## <span data-ttu-id="c6aa4-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6aa4-134">NOTES</span></span>

## <span data-ttu-id="c6aa4-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6aa4-135">RELATED LINKS</span></span>

