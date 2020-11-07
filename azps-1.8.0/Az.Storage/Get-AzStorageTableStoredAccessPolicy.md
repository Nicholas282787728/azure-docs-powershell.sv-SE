---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: f66fc4a0581d41b7746322dd8fe9ffe8bb8b50e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746366"
---
# <span data-ttu-id="e151e-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e151e-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="e151e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e151e-102">SYNOPSIS</span></span>
<span data-ttu-id="e151e-103">Hämtar den lagrade åtkomst principen för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="e151e-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="e151e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e151e-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e151e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e151e-105">DESCRIPTION</span></span>
<span data-ttu-id="e151e-106">Cmdleten **Get-AzStorageTableStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="e151e-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="e151e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e151e-107">EXAMPLES</span></span>

### <span data-ttu-id="e151e-108">Exempel 1: Hämta en lagrad åtkomst princip i en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="e151e-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="e151e-109">Det här kommandot får åtkomst principen med namnet Policy50 i lagrings tabellen med namnet Table02.</span><span class="sxs-lookup"><span data-stu-id="e151e-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="e151e-110">Exempel 2: Hämta alla lagrade åtkomst principer i en lagrings tabell</span><span class="sxs-lookup"><span data-stu-id="e151e-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="e151e-111">Det här kommandot får alla åtkomst principer i tabellen som heter Table02.</span><span class="sxs-lookup"><span data-stu-id="e151e-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="e151e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e151e-112">PARAMETERS</span></span>

### <span data-ttu-id="e151e-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e151e-113">-Context</span></span>
<span data-ttu-id="e151e-114">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="e151e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e151e-115">Använd New-AzStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="e151e-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e151e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e151e-116">-DefaultProfile</span></span>
<span data-ttu-id="e151e-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e151e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e151e-118">-Princip</span><span class="sxs-lookup"><span data-stu-id="e151e-118">-Policy</span></span>
<span data-ttu-id="e151e-119">Anger en lagrad åtkomst princip som innehåller behörigheter för denna delade Access-signatur (SAS).</span><span class="sxs-lookup"><span data-stu-id="e151e-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e151e-120">-Tabell</span><span class="sxs-lookup"><span data-stu-id="e151e-120">-Table</span></span>
<span data-ttu-id="e151e-121">Anger namnet på Azure Storage-tabellen.</span><span class="sxs-lookup"><span data-stu-id="e151e-121">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e151e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e151e-122">CommonParameters</span></span>
<span data-ttu-id="e151e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e151e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e151e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e151e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e151e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e151e-125">INPUTS</span></span>

### <span data-ttu-id="e151e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e151e-126">System.String</span></span>

### <span data-ttu-id="e151e-127">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e151e-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e151e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e151e-128">OUTPUTS</span></span>

### <span data-ttu-id="e151e-129">Microsoft. WindowsAzure. Storage. Table. SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="e151e-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="e151e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e151e-130">NOTES</span></span>

## <span data-ttu-id="e151e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e151e-131">RELATED LINKS</span></span>

[<span data-ttu-id="e151e-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e151e-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="e151e-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e151e-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="e151e-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e151e-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="e151e-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e151e-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


