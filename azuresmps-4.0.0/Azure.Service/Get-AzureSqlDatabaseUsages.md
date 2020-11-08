---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 9953AF91-2424-4BD1-9133-E0E07AC1087E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a17ff5e4ec976fcf0c6be02e3fbc373d7ffd2f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099793"
---
# <span data-ttu-id="b24b1-101">Get-AzureSqlDatabaseUsages</span><span class="sxs-lookup"><span data-stu-id="b24b1-101">Get-AzureSqlDatabaseUsages</span></span>

## <span data-ttu-id="b24b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b24b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b24b1-103">Hämtar storlek och storlek på en SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="b24b1-103">Gets the size and size limit of a SQL Database.</span></span>

## <span data-ttu-id="b24b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b24b1-104">SYNTAX</span></span>

```
Get-AzureSqlDatabaseUsages -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b24b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b24b1-105">DESCRIPTION</span></span>
<span data-ttu-id="b24b1-106">Cmdleten **Get-AzureSqlDatabaseUsages** får den aktuella storleken och storleken på en Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="b24b1-106">The **Get-AzureSqlDatabaseUsages** cmdlet gets the current size and size limit of an Azure SQL Database.</span></span>

## <span data-ttu-id="b24b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b24b1-107">EXAMPLES</span></span>

### <span data-ttu-id="b24b1-108">Exempel 1: Hämta information om användning för en SQL-databas</span><span class="sxs-lookup"><span data-stu-id="b24b1-108">Example 1: Get usage information for a SQL Database</span></span>
```
PS C:\> Get-AzureSqlDatabaseUsages -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b24b1-109">Det här kommandot får information om storlek och storleks gräns för SQL-databasen med namnet Database01 på Server01.</span><span class="sxs-lookup"><span data-stu-id="b24b1-109">This command gets the size and size limit information for the SQL Database named Database01 on Server01.</span></span>

## <span data-ttu-id="b24b1-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b24b1-110">PARAMETERS</span></span>

### <span data-ttu-id="b24b1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b24b1-111">-DatabaseName</span></span>
<span data-ttu-id="b24b1-112">Anger namnet på din Azure SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="b24b1-112">Specifies the name of the Azure SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b24b1-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="b24b1-113">-Profile</span></span>
<span data-ttu-id="b24b1-114">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="b24b1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b24b1-115">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="b24b1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b24b1-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b24b1-116">-ServerName</span></span>
<span data-ttu-id="b24b1-117">Anger namnet på den server som är värd för Azure SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="b24b1-117">Specifies the name of the server that hosts the Azure SQL Database.</span></span>

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

### <span data-ttu-id="b24b1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24b1-118">CommonParameters</span></span>
<span data-ttu-id="b24b1-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24b1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24b1-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b24b1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24b1-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b24b1-121">INPUTS</span></span>

## <span data-ttu-id="b24b1-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b24b1-122">OUTPUTS</span></span>

## <span data-ttu-id="b24b1-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b24b1-123">NOTES</span></span>

## <span data-ttu-id="b24b1-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b24b1-124">RELATED LINKS</span></span>

