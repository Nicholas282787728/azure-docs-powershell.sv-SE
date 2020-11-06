---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572192"
---
# <span data-ttu-id="4d0a8-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4d0a8-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="4d0a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d0a8-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0a8-103">Skapar en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-103">Creates a storage table.</span></span>

## <span data-ttu-id="4d0a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d0a8-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="4d0a8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d0a8-105">DESCRIPTION</span></span>
<span data-ttu-id="4d0a8-106">Cmdleten **New-AzureStorageTable** skapar en lagrings tabell som är kopplad till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="4d0a8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d0a8-107">EXAMPLES</span></span>

### <span data-ttu-id="4d0a8-108">Exempel 1: skapa en Azure Storage-tabell</span><span class="sxs-lookup"><span data-stu-id="4d0a8-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="4d0a8-109">Det här kommandot skapar en lagrings tabell med namnet tableabc.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="4d0a8-110">Exempel 2: skapa flera Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="4d0a8-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="4d0a8-111">Det här kommandot skapar flera tabeller.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-111">This command creates multiple tables.</span></span>
<span data-ttu-id="4d0a8-112">Den använder metoden **Split** i **klassen .net och** skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="4d0a8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d0a8-113">PARAMETERS</span></span>

### <span data-ttu-id="4d0a8-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4d0a8-114">-Context</span></span>
<span data-ttu-id="4d0a8-115">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-115">Specifies the storage context.</span></span>
<span data-ttu-id="4d0a8-116">För att skapa den kan du använda New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4d0a8-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d0a8-117">-Name</span></span>
<span data-ttu-id="4d0a8-118">Anger ett namn för den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d0a8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0a8-119">CommonParameters</span></span>
<span data-ttu-id="4d0a8-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d0a8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0a8-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d0a8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0a8-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d0a8-122">INPUTS</span></span>

## <span data-ttu-id="4d0a8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d0a8-123">OUTPUTS</span></span>

## <span data-ttu-id="4d0a8-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d0a8-124">NOTES</span></span>

## <span data-ttu-id="4d0a8-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d0a8-125">RELATED LINKS</span></span>

[<span data-ttu-id="4d0a8-126">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4d0a8-126">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="4d0a8-127">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="4d0a8-127">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


