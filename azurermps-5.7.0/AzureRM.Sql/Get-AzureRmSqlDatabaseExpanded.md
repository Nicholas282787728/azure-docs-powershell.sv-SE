---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 952967EB-AEAD-4597-B837-6669CE73739E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseexpanded
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseExpanded.md
ms.openlocfilehash: 472e8e7a2f0919115686764136b6b40f5e1da913
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576400"
---
# <span data-ttu-id="63b64-101">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="63b64-101">Get-AzureRmSqlDatabaseExpanded</span></span>

## <span data-ttu-id="63b64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63b64-102">SYNOPSIS</span></span>
<span data-ttu-id="63b64-103">Hämtar en databas och dess utökade egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="63b64-103">Gets a database and its expanded property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63b64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63b64-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseExpanded [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63b64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63b64-105">DESCRIPTION</span></span>
<span data-ttu-id="63b64-106">Cmdleten **Get-AzureRmSqlDatabaseExpanded** hämtar en databas och dess utökade egenskaps värden.</span><span class="sxs-lookup"><span data-stu-id="63b64-106">The **Get-AzureRmSqlDatabaseExpanded** cmdlet gets a database and its expanded property values.</span></span>

<span data-ttu-id="63b64-107">Denna cmdlet stöds också av SQL Server utsträckt databas tjänst på Azure.</span><span class="sxs-lookup"><span data-stu-id="63b64-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="63b64-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63b64-108">EXAMPLES</span></span>

### <span data-ttu-id="63b64-109">Exempel 1: Hämta databas objekt med information om tjänst nivå klassificering</span><span class="sxs-lookup"><span data-stu-id="63b64-109">Example 1: Get database object that has service tier advisor information</span></span>
```
PS C:\>Get-AzureSqlDatabaseExpanded -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="63b64-110">Det här kommandot returnerar den databas som har utökade egenskaper som innehåller information om tjänst nivå klassificering.</span><span class="sxs-lookup"><span data-stu-id="63b64-110">This command returns the database that has expanded properties that contain the service tier advisor information.</span></span>

## <span data-ttu-id="63b64-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63b64-111">PARAMETERS</span></span>

### <span data-ttu-id="63b64-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63b64-112">-DatabaseName</span></span>
<span data-ttu-id="63b64-113">Anger namnet på den databas som ska visas.</span><span class="sxs-lookup"><span data-stu-id="63b64-113">Specifies the name of the database to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63b64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63b64-114">-DefaultProfile</span></span>
<span data-ttu-id="63b64-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="63b64-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63b64-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63b64-116">-ResourceGroupName</span></span>
<span data-ttu-id="63b64-117">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="63b64-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="63b64-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="63b64-118">-ServerName</span></span>
<span data-ttu-id="63b64-119">Anger namnet på den server som är värd för databasen.</span><span class="sxs-lookup"><span data-stu-id="63b64-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="63b64-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63b64-120">-Confirm</span></span>
<span data-ttu-id="63b64-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63b64-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63b64-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63b64-122">-WhatIf</span></span>
<span data-ttu-id="63b64-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="63b64-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63b64-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="63b64-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63b64-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63b64-125">CommonParameters</span></span>
<span data-ttu-id="63b64-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63b64-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63b64-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63b64-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63b64-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63b64-128">INPUTS</span></span>

### <span data-ttu-id="63b64-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="63b64-129">None</span></span>
<span data-ttu-id="63b64-130">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="63b64-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="63b64-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63b64-131">OUTPUTS</span></span>

## <span data-ttu-id="63b64-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63b64-132">NOTES</span></span>

## <span data-ttu-id="63b64-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63b64-133">RELATED LINKS</span></span>

[<span data-ttu-id="63b64-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="63b64-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
