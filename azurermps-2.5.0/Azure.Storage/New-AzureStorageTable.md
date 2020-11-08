---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: 4fe02c9824945593de4b4160e9db10b1573a335a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930018"
---
# <span data-ttu-id="12b42-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="12b42-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="12b42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="12b42-102">SYNOPSIS</span></span>
<span data-ttu-id="12b42-103">Skapar en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="12b42-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12b42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="12b42-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12b42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="12b42-105">DESCRIPTION</span></span>
<span data-ttu-id="12b42-106">Cmdleten **New-AzureStorageTable** skapar en lagrings tabell som är kopplad till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="12b42-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="12b42-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="12b42-107">EXAMPLES</span></span>

### <span data-ttu-id="12b42-108">Exempel 1: skapa en Azure Storage-tabell</span><span class="sxs-lookup"><span data-stu-id="12b42-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="12b42-109">Det här kommandot skapar en lagrings tabell med namnet tableabc.</span><span class="sxs-lookup"><span data-stu-id="12b42-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="12b42-110">Exempel 2: skapa flera Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="12b42-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="12b42-111">Det här kommandot skapar flera tabeller.</span><span class="sxs-lookup"><span data-stu-id="12b42-111">This command creates multiple tables.</span></span>
<span data-ttu-id="12b42-112">Den använder metoden **Split** i **klassen .net och** skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="12b42-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="12b42-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="12b42-113">PARAMETERS</span></span>

### <span data-ttu-id="12b42-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="12b42-114">-Context</span></span>
<span data-ttu-id="12b42-115">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="12b42-115">Specifies the storage context.</span></span>
<span data-ttu-id="12b42-116">För att skapa den kan du använda New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b42-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12b42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b42-117">-DefaultProfile</span></span>
<span data-ttu-id="12b42-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="12b42-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12b42-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="12b42-119">-Name</span></span>
<span data-ttu-id="12b42-120">Anger ett namn för den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="12b42-120">Specifies a name for the new table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12b42-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b42-121">CommonParameters</span></span>
<span data-ttu-id="12b42-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b42-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b42-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b42-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b42-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="12b42-124">INPUTS</span></span>

### <span data-ttu-id="12b42-125">System. String</span><span class="sxs-lookup"><span data-stu-id="12b42-125">System.String</span></span>

### <span data-ttu-id="12b42-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="12b42-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="12b42-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="12b42-127">OUTPUTS</span></span>

### <span data-ttu-id="12b42-128">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="12b42-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="12b42-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="12b42-129">NOTES</span></span>

## <span data-ttu-id="12b42-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="12b42-130">RELATED LINKS</span></span>

[<span data-ttu-id="12b42-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="12b42-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="12b42-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="12b42-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)

