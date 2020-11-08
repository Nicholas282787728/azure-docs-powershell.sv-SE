---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTable.md
ms.openlocfilehash: 0f46570858368a821d176a5f4e0a907c8a56b49c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94100743"
---
# <span data-ttu-id="a9db8-101">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a9db8-101">New-AzStorageTable</span></span>

## <span data-ttu-id="a9db8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9db8-102">SYNOPSIS</span></span>
<span data-ttu-id="a9db8-103">Skapar en lagrings tabell.</span><span class="sxs-lookup"><span data-stu-id="a9db8-103">Creates a storage table.</span></span>

## <span data-ttu-id="a9db8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9db8-104">SYNTAX</span></span>

```
New-AzStorageTable [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9db8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9db8-105">DESCRIPTION</span></span>
<span data-ttu-id="a9db8-106">Cmdleten **New-AzStorageTable** skapar en lagrings tabell som är kopplad till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="a9db8-106">The **New-AzStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="a9db8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9db8-107">EXAMPLES</span></span>

### <span data-ttu-id="a9db8-108">Exempel 1: skapa en Azure Storage-tabell</span><span class="sxs-lookup"><span data-stu-id="a9db8-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzStorageTable -Name "tableabc"
```

<span data-ttu-id="a9db8-109">Det här kommandot skapar en lagrings tabell med namnet tableabc.</span><span class="sxs-lookup"><span data-stu-id="a9db8-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="a9db8-110">Exempel 2: skapa flera Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="a9db8-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzStorageTable
```

<span data-ttu-id="a9db8-111">Det här kommandot skapar flera tabeller.</span><span class="sxs-lookup"><span data-stu-id="a9db8-111">This command creates multiple tables.</span></span>
<span data-ttu-id="a9db8-112">Den använder metoden **Split** i **klassen .net och** skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="a9db8-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a9db8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9db8-113">PARAMETERS</span></span>

### <span data-ttu-id="a9db8-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a9db8-114">-Context</span></span>
<span data-ttu-id="a9db8-115">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="a9db8-115">Specifies the storage context.</span></span>
<span data-ttu-id="a9db8-116">För att skapa den kan du använda New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9db8-116">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a9db8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9db8-117">-DefaultProfile</span></span>
<span data-ttu-id="a9db8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9db8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9db8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9db8-119">-Name</span></span>
<span data-ttu-id="a9db8-120">Anger ett namn för den nya tabellen.</span><span class="sxs-lookup"><span data-stu-id="a9db8-120">Specifies a name for the new table.</span></span>

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

### <span data-ttu-id="a9db8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9db8-121">CommonParameters</span></span>
<span data-ttu-id="a9db8-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9db8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9db8-123">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9db8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9db8-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9db8-124">INPUTS</span></span>

### <span data-ttu-id="a9db8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a9db8-125">System.String</span></span>

### <span data-ttu-id="a9db8-126">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a9db8-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a9db8-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9db8-127">OUTPUTS</span></span>

### <span data-ttu-id="a9db8-128">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="a9db8-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="a9db8-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9db8-129">NOTES</span></span>

## <span data-ttu-id="a9db8-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9db8-130">RELATED LINKS</span></span>

[<span data-ttu-id="a9db8-131">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a9db8-131">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)

[<span data-ttu-id="a9db8-132">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="a9db8-132">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


