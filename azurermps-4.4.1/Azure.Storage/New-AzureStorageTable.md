---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 2f051fb0724ac266753d87fc30489398a4aa64a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575074"
---
# <span data-ttu-id="d8df0-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d8df0-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="d8df0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8df0-102">SYNOPSIS</span></span>
<span data-ttu-id="d8df0-103">Skapar en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="d8df0-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8df0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8df0-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d8df0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8df0-105">DESCRIPTION</span></span>
<span data-ttu-id="d8df0-106">Cmdleten **New-AzureStorageTable** skapar en lagrings tabell som är kopplad till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="d8df0-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="d8df0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8df0-107">EXAMPLES</span></span>

### <span data-ttu-id="d8df0-108">Exempel 1: skapa en Azure Storage-tabell</span><span class="sxs-lookup"><span data-stu-id="d8df0-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="d8df0-109">Det här kommandot skapar en lagrings tabell med namnet tableabc.</span><span class="sxs-lookup"><span data-stu-id="d8df0-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="d8df0-110">Exempel 2: skapa flera Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="d8df0-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="d8df0-111">Det här kommandot skapar flera tabeller.</span><span class="sxs-lookup"><span data-stu-id="d8df0-111">This command creates multiple tables.</span></span>
<span data-ttu-id="d8df0-112">Den använder metoden **Split** i **klassen .net och** skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="d8df0-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="d8df0-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8df0-113">PARAMETERS</span></span>

### <span data-ttu-id="d8df0-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d8df0-114">-Context</span></span>
<span data-ttu-id="d8df0-115">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="d8df0-115">Specifies the storage context.</span></span>
<span data-ttu-id="d8df0-116">För att skapa den kan du använda New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8df0-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d8df0-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8df0-117">-Name</span></span>
<span data-ttu-id="d8df0-118">Anger ett namn för den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="d8df0-118">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="d8df0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8df0-119">CommonParameters</span></span>
<span data-ttu-id="d8df0-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8df0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8df0-121">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8df0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8df0-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8df0-122">INPUTS</span></span>

### <span data-ttu-id="d8df0-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8df0-123">IStorageContext</span></span>

<span data-ttu-id="d8df0-124">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d8df0-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d8df0-125">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="d8df0-125">String</span></span>

<span data-ttu-id="d8df0-126">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="d8df0-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d8df0-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8df0-127">OUTPUTS</span></span>

### <span data-ttu-id="d8df0-128">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d8df0-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="d8df0-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8df0-129">NOTES</span></span>

## <span data-ttu-id="d8df0-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8df0-130">RELATED LINKS</span></span>

[<span data-ttu-id="d8df0-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d8df0-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="d8df0-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d8df0-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)

