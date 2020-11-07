---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 29b2bb0c6a9c6e8e34c08a7ce04ca1c3ed071c84
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923553"
---
# <span data-ttu-id="6ce5d-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="6ce5d-101">New-AzStorageTable</span></span>

## <span data-ttu-id="6ce5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ce5d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce5d-103">Skapar en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-103">Creates a storage table.</span></span>

## <span data-ttu-id="6ce5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ce5d-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ce5d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ce5d-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce5d-106">Cmdleten **New-AzStorageTable** skapar en lagrings tabell som är kopplad till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="6ce5d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ce5d-107">EXAMPLES</span></span>

### <span data-ttu-id="6ce5d-108">Exempel 1: skapa en Azure Storage-tabell</span><span class="sxs-lookup"><span data-stu-id="6ce5d-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="6ce5d-109">Det här kommandot skapar en lagrings tabell med namnet tableabc.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="6ce5d-110">Exempel 2: skapa flera Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="6ce5d-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="6ce5d-111">Det här kommandot skapar flera tabeller.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-111">This command creates multiple tables.</span></span>
<span data-ttu-id="6ce5d-112">Den använder metoden **Split** i **klassen .net och** skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="6ce5d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ce5d-113">PARAMETERS</span></span>

### <span data-ttu-id="6ce5d-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6ce5d-114">-Context</span></span>
<span data-ttu-id="6ce5d-115">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-115">Specifies the storage context.</span></span>
<span data-ttu-id="6ce5d-116">För att skapa den kan du använda New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6ce5d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce5d-117">-DefaultProfile</span></span>
<span data-ttu-id="6ce5d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ce5d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="6ce5d-119">-Name</span></span>
<span data-ttu-id="6ce5d-120">Anger ett namn för den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="6ce5d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce5d-121">CommonParameters</span></span>
<span data-ttu-id="6ce5d-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ce5d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce5d-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce5d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce5d-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ce5d-124">INPUTS</span></span>

### <span data-ttu-id="6ce5d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6ce5d-125">System.String</span></span>

### <span data-ttu-id="6ce5d-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ce5d-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6ce5d-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ce5d-127">OUTPUTS</span></span>

### <span data-ttu-id="6ce5d-128">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="6ce5d-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="6ce5d-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ce5d-129">NOTES</span></span>

## <span data-ttu-id="6ce5d-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ce5d-130">RELATED LINKS</span></span>

[<span data-ttu-id="6ce5d-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="6ce5d-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="6ce5d-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="6ce5d-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


