---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572343"
---
# <span data-ttu-id="fb221-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="fb221-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="fb221-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb221-102">SYNOPSIS</span></span>
<span data-ttu-id="fb221-103">Visar lagrings tabellerna.</span><span class="sxs-lookup"><span data-stu-id="fb221-103">Lists the storage tables.</span></span>

## <span data-ttu-id="fb221-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb221-104">SYNTAX</span></span>

### <span data-ttu-id="fb221-105">TableName (standard)</span><span class="sxs-lookup"><span data-stu-id="fb221-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="fb221-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="fb221-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="fb221-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb221-107">DESCRIPTION</span></span>
<span data-ttu-id="fb221-108">Cmdleten **Get-AzureStorageTable** innehåller lagrings tabeller som är kopplade till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="fb221-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="fb221-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb221-109">EXAMPLES</span></span>

### <span data-ttu-id="fb221-110">Exempel 1: lista alla Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="fb221-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="fb221-111">Det här kommandot hämtar alla lagrings tabeller för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="fb221-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="fb221-112">Exempel 2: lista Azure Storage-tabeller med ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="fb221-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="fb221-113">Det här kommandot använder ett jokertecken för att hämta lagrings tabeller vars namn börjar med tabellen.</span><span class="sxs-lookup"><span data-stu-id="fb221-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="fb221-114">Exempel 3: lista Azure Storage-tabeller med hjälp av tabell namns prefix</span><span class="sxs-lookup"><span data-stu-id="fb221-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="fb221-115">Det här kommandot använder parametern *prefix* för att hämta lagrings tabeller vars namn börjar med tabellen.</span><span class="sxs-lookup"><span data-stu-id="fb221-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="fb221-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb221-116">PARAMETERS</span></span>

### <span data-ttu-id="fb221-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="fb221-117">-Context</span></span>
<span data-ttu-id="fb221-118">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="fb221-118">Specifies the storage context.</span></span>
<span data-ttu-id="fb221-119">För att skapa den kan du använda New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb221-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb221-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb221-120">-Name</span></span>
<span data-ttu-id="fb221-121">Anger tabell namnet.</span><span class="sxs-lookup"><span data-stu-id="fb221-121">Specifies the table name.</span></span>
<span data-ttu-id="fb221-122">Om tabell namnet är tomt visar cmdleten alla tabeller.</span><span class="sxs-lookup"><span data-stu-id="fb221-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="fb221-123">Annars visas alla tabeller som matchar det angivna namnet eller det vanliga namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="fb221-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb221-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="fb221-124">-Prefix</span></span>
<span data-ttu-id="fb221-125">Anger ett prefix som används i namnet på den eller de tabeller som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="fb221-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="fb221-126">Du kan använda den här för att hitta alla tabeller som börjar med samma sträng, till exempel tabell.</span><span class="sxs-lookup"><span data-stu-id="fb221-126">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb221-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb221-127">CommonParameters</span></span>
<span data-ttu-id="fb221-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb221-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb221-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb221-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb221-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb221-130">INPUTS</span></span>

## <span data-ttu-id="fb221-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb221-131">OUTPUTS</span></span>

## <span data-ttu-id="fb221-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb221-132">NOTES</span></span>

## <span data-ttu-id="fb221-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb221-133">RELATED LINKS</span></span>

[<span data-ttu-id="fb221-134">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="fb221-134">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="fb221-135">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="fb221-135">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


