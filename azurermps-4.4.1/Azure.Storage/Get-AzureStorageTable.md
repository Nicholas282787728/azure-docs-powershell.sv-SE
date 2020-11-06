---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573805"
---
# <span data-ttu-id="c6c16-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="c6c16-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="c6c16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6c16-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c16-103">Visar lagrings tabellerna.</span><span class="sxs-lookup"><span data-stu-id="c6c16-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6c16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6c16-104">SYNTAX</span></span>

### <span data-ttu-id="c6c16-105">TableName (standard)</span><span class="sxs-lookup"><span data-stu-id="c6c16-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="c6c16-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="c6c16-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="c6c16-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6c16-107">DESCRIPTION</span></span>
<span data-ttu-id="c6c16-108">Cmdleten **Get-AzureStorageTable** innehåller lagrings tabeller som är kopplade till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="c6c16-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="c6c16-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6c16-109">EXAMPLES</span></span>

### <span data-ttu-id="c6c16-110">Exempel 1: lista alla Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="c6c16-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="c6c16-111">Det här kommandot hämtar alla lagrings tabeller för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="c6c16-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="c6c16-112">Exempel 2: lista Azure Storage-tabeller med ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="c6c16-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="c6c16-113">Det här kommandot använder ett jokertecken för att hämta lagrings tabeller vars namn börjar med tabellen.</span><span class="sxs-lookup"><span data-stu-id="c6c16-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="c6c16-114">Exempel 3: lista Azure Storage-tabeller med hjälp av tabell namns prefix</span><span class="sxs-lookup"><span data-stu-id="c6c16-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="c6c16-115">Det här kommandot använder parametern *prefix* för att hämta lagrings tabeller vars namn börjar med tabellen.</span><span class="sxs-lookup"><span data-stu-id="c6c16-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="c6c16-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6c16-116">PARAMETERS</span></span>

### <span data-ttu-id="c6c16-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c6c16-117">-Context</span></span>
<span data-ttu-id="c6c16-118">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="c6c16-118">Specifies the storage context.</span></span>
<span data-ttu-id="c6c16-119">För att skapa den kan du använda New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6c16-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c6c16-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6c16-120">-Name</span></span>
<span data-ttu-id="c6c16-121">Anger tabell namnet.</span><span class="sxs-lookup"><span data-stu-id="c6c16-121">Specifies the table name.</span></span>
<span data-ttu-id="c6c16-122">Om tabell namnet är tomt visar cmdleten alla tabeller.</span><span class="sxs-lookup"><span data-stu-id="c6c16-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="c6c16-123">Annars visas alla tabeller som matchar det angivna namnet eller det vanliga namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="c6c16-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="c6c16-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="c6c16-124">-Prefix</span></span>
<span data-ttu-id="c6c16-125">Anger ett prefix som används i namnet på den eller de tabeller som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="c6c16-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="c6c16-126">Du kan använda den här för att hitta alla tabeller som börjar med samma sträng, till exempel tabell.</span><span class="sxs-lookup"><span data-stu-id="c6c16-126">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="c6c16-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c16-127">CommonParameters</span></span>
<span data-ttu-id="c6c16-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6c16-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c16-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c16-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c16-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6c16-130">INPUTS</span></span>

### <span data-ttu-id="c6c16-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6c16-131">IStorageContext</span></span>

<span data-ttu-id="c6c16-132">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="c6c16-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c6c16-133">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="c6c16-133">String</span></span>

<span data-ttu-id="c6c16-134">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="c6c16-134">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c6c16-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6c16-135">OUTPUTS</span></span>

### <span data-ttu-id="c6c16-136">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="c6c16-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="c6c16-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6c16-137">NOTES</span></span>

## <span data-ttu-id="c6c16-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6c16-138">RELATED LINKS</span></span>

[<span data-ttu-id="c6c16-139">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="c6c16-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="c6c16-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="c6c16-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


