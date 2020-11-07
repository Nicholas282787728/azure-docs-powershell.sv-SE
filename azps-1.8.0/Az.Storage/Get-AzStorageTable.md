---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTable.md
ms.openlocfilehash: 5c575ace97687ca6906a73e8e79d93343f369f45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746369"
---
# <span data-ttu-id="04a79-101">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="04a79-101">Get-AzStorageTable</span></span>

## <span data-ttu-id="04a79-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04a79-102">SYNOPSIS</span></span>
<span data-ttu-id="04a79-103">Visar lagrings tabellerna.</span><span class="sxs-lookup"><span data-stu-id="04a79-103">Lists the storage tables.</span></span>

## <span data-ttu-id="04a79-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04a79-104">SYNTAX</span></span>

### <span data-ttu-id="04a79-105">TableName (standard)</span><span class="sxs-lookup"><span data-stu-id="04a79-105">TableName (Default)</span></span>
```
Get-AzStorageTable [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04a79-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="04a79-106">TablePrefix</span></span>
```
Get-AzStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04a79-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04a79-107">DESCRIPTION</span></span>
<span data-ttu-id="04a79-108">Cmdleten **Get-AzStorageTable** innehåller lagrings tabeller som är kopplade till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="04a79-108">The **Get-AzStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="04a79-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04a79-109">EXAMPLES</span></span>

### <span data-ttu-id="04a79-110">Exempel 1: lista alla Azure Storage-tabeller</span><span class="sxs-lookup"><span data-stu-id="04a79-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzStorageTable
```

<span data-ttu-id="04a79-111">Det här kommandot hämtar alla lagrings tabeller för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="04a79-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="04a79-112">Exempel 2: lista Azure Storage-tabeller med ett jokertecken</span><span class="sxs-lookup"><span data-stu-id="04a79-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzStorageTable -Name table*
```

<span data-ttu-id="04a79-113">Det här kommandot använder ett jokertecken för att hämta lagrings tabeller vars namn börjar med tabellen.</span><span class="sxs-lookup"><span data-stu-id="04a79-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="04a79-114">Exempel 3: lista Azure Storage-tabeller med hjälp av tabell namns prefix</span><span class="sxs-lookup"><span data-stu-id="04a79-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzStorageTable -Prefix "table"
```

<span data-ttu-id="04a79-115">Det här kommandot använder parametern *prefix* för att hämta lagrings tabeller vars namn börjar med tabellen.</span><span class="sxs-lookup"><span data-stu-id="04a79-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="04a79-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04a79-116">PARAMETERS</span></span>

### <span data-ttu-id="04a79-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="04a79-117">-Context</span></span>
<span data-ttu-id="04a79-118">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="04a79-118">Specifies the storage context.</span></span>
<span data-ttu-id="04a79-119">För att skapa den kan du använda New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04a79-119">To create it, you can use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="04a79-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a79-120">-DefaultProfile</span></span>
<span data-ttu-id="04a79-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04a79-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04a79-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="04a79-122">-Name</span></span>
<span data-ttu-id="04a79-123">Anger tabell namnet.</span><span class="sxs-lookup"><span data-stu-id="04a79-123">Specifies the table name.</span></span>
<span data-ttu-id="04a79-124">Om tabell namnet är tomt visar cmdleten alla tabeller.</span><span class="sxs-lookup"><span data-stu-id="04a79-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="04a79-125">Annars visas alla tabeller som matchar det angivna namnet eller det vanliga namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="04a79-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="04a79-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="04a79-126">-Prefix</span></span>
<span data-ttu-id="04a79-127">Anger ett prefix som används i namnet på den eller de tabeller som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="04a79-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="04a79-128">Du kan använda den här för att hitta alla tabeller som börjar med samma sträng, till exempel tabell.</span><span class="sxs-lookup"><span data-stu-id="04a79-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="04a79-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a79-129">CommonParameters</span></span>
<span data-ttu-id="04a79-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04a79-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a79-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a79-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a79-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04a79-132">INPUTS</span></span>

### <span data-ttu-id="04a79-133">System. String</span><span class="sxs-lookup"><span data-stu-id="04a79-133">System.String</span></span>

### <span data-ttu-id="04a79-134">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="04a79-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04a79-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04a79-135">OUTPUTS</span></span>

### <span data-ttu-id="04a79-136">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="04a79-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="04a79-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04a79-137">NOTES</span></span>

## <span data-ttu-id="04a79-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04a79-138">RELATED LINKS</span></span>

[<span data-ttu-id="04a79-139">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="04a79-139">New-AzStorageTable</span></span>](./New-AzStorageTable.md)

[<span data-ttu-id="04a79-140">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="04a79-140">Remove-AzStorageTable</span></span>](./Remove-AzStorageTable.md)


