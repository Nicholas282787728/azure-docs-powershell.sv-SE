---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 1b01550e8501a0a7f81ac5c04cd0083fc521fec5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746320"
---
# <span data-ttu-id="272ed-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="272ed-101">New-AzStorageTable</span></span>

## <span data-ttu-id="272ed-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="272ed-102">SYNOPSIS</span></span>
<span data-ttu-id="272ed-103">Skapar en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="272ed-103">Creates a storage table.</span></span>

## <span data-ttu-id="272ed-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="272ed-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="272ed-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="272ed-105">DESCRIPTION</span></span>
<span data-ttu-id="272ed-106">Cmdleten **New-AzStorageTable** skapar en lagrings tabell som är kopplad till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="272ed-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="272ed-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="272ed-107">EXAMPLES</span></span>

### <span data-ttu-id="272ed-108">Exempel 1: skapa en Azure Storage-tabell</span><span class="sxs-lookup"><span data-stu-id="272ed-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="272ed-109">Det här kommandot skapar en lagrings tabell med namnet tableabc.</span><span class="sxs-lookup"><span data-stu-id="272ed-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="272ed-110">Exempel 2: skapa flera Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="272ed-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="272ed-111">Det här kommandot skapar flera tabeller.</span><span class="sxs-lookup"><span data-stu-id="272ed-111">This command creates multiple tables.</span></span>
<span data-ttu-id="272ed-112">Den använder metoden **Split** i **klassen .net och** skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="272ed-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="272ed-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="272ed-113">PARAMETERS</span></span>

### <span data-ttu-id="272ed-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="272ed-114">-Context</span></span>
<span data-ttu-id="272ed-115">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="272ed-115">Specifies the storage context.</span></span>
<span data-ttu-id="272ed-116">För att skapa den kan du använda New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="272ed-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="272ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272ed-117">-DefaultProfile</span></span>
<span data-ttu-id="272ed-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="272ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ed-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="272ed-119">-Name</span></span>
<span data-ttu-id="272ed-120">Anger ett namn för den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="272ed-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="272ed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272ed-121">CommonParameters</span></span>
<span data-ttu-id="272ed-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="272ed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272ed-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="272ed-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272ed-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="272ed-124">INPUTS</span></span>

### <span data-ttu-id="272ed-125">System. String</span><span class="sxs-lookup"><span data-stu-id="272ed-125">System.String</span></span>

### <span data-ttu-id="272ed-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="272ed-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="272ed-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="272ed-127">OUTPUTS</span></span>

### <span data-ttu-id="272ed-128">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="272ed-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="272ed-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="272ed-129">NOTES</span></span>

## <span data-ttu-id="272ed-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="272ed-130">RELATED LINKS</span></span>

[<span data-ttu-id="272ed-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="272ed-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="272ed-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="272ed-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


