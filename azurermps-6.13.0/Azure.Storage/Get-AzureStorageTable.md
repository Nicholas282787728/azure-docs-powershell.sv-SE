---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
ms.openlocfilehash: 1d31bff44bb93db1022a88a464c2942a2a3fadbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757163"
---
# <span data-ttu-id="3e01e-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3e01e-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="3e01e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e01e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e01e-103">Visar lagrings tabellerna.</span><span class="sxs-lookup"><span data-stu-id="3e01e-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e01e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e01e-104">SYNTAX</span></span>

### <span data-ttu-id="3e01e-105">TableName (standard)</span><span class="sxs-lookup"><span data-stu-id="3e01e-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e01e-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="3e01e-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e01e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e01e-107">DESCRIPTION</span></span>
<span data-ttu-id="3e01e-108">Cmdleten **Get-AzureStorageTable** innehåller lagrings tabeller som är kopplade till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="3e01e-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="3e01e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e01e-109">EXAMPLES</span></span>

### <span data-ttu-id="3e01e-110">Exempel 1: lista alla Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="3e01e-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="3e01e-111">Det här kommandot hämtar alla lagrings tabeller för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="3e01e-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="3e01e-112">Exempel 2: lista Azure Storage-tabeller med ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="3e01e-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="3e01e-113">Det här kommandot använder ett jokertecken för att hämta lagrings tabeller vars namn börjar med tabellen.</span><span class="sxs-lookup"><span data-stu-id="3e01e-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="3e01e-114">Exempel 3: lista Azure Storage-tabeller med hjälp av tabell namns prefix</span><span class="sxs-lookup"><span data-stu-id="3e01e-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="3e01e-115">Det här kommandot använder parametern *prefix* för att hämta lagrings tabeller vars namn börjar med tabellen.</span><span class="sxs-lookup"><span data-stu-id="3e01e-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="3e01e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e01e-116">PARAMETERS</span></span>

### <span data-ttu-id="3e01e-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3e01e-117">-Context</span></span>
<span data-ttu-id="3e01e-118">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="3e01e-118">Specifies the storage context.</span></span>
<span data-ttu-id="3e01e-119">För att skapa den kan du använda New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e01e-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3e01e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e01e-120">-DefaultProfile</span></span>
<span data-ttu-id="3e01e-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e01e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e01e-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e01e-122">-Name</span></span>
<span data-ttu-id="3e01e-123">Anger tabell namnet.</span><span class="sxs-lookup"><span data-stu-id="3e01e-123">Specifies the table name.</span></span>
<span data-ttu-id="3e01e-124">Om tabell namnet är tomt visar cmdleten alla tabeller.</span><span class="sxs-lookup"><span data-stu-id="3e01e-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="3e01e-125">Annars visas alla tabeller som matchar det angivna namnet eller det vanliga namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="3e01e-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e01e-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="3e01e-126">-Prefix</span></span>
<span data-ttu-id="3e01e-127">Anger ett prefix som används i namnet på den eller de tabeller som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="3e01e-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="3e01e-128">Du kan använda den här för att hitta alla tabeller som börjar med samma sträng, till exempel tabell.</span><span class="sxs-lookup"><span data-stu-id="3e01e-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e01e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e01e-129">CommonParameters</span></span>
<span data-ttu-id="3e01e-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e01e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e01e-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e01e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e01e-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e01e-132">INPUTS</span></span>

### <span data-ttu-id="3e01e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3e01e-133">System.String</span></span>

### <span data-ttu-id="3e01e-134">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3e01e-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3e01e-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e01e-135">OUTPUTS</span></span>

### <span data-ttu-id="3e01e-136">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3e01e-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="3e01e-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e01e-137">NOTES</span></span>

## <span data-ttu-id="3e01e-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e01e-138">RELATED LINKS</span></span>

[<span data-ttu-id="3e01e-139">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3e01e-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="3e01e-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3e01e-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)

