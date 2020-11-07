---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: be32e761fc854c6ad4a270f36e4c9b6328e00ba1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923706"
---
# <span data-ttu-id="947aa-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="947aa-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="947aa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="947aa-102">SYNOPSIS</span></span>
<span data-ttu-id="947aa-103">Hämtar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="947aa-103">Gets a Storage account.</span></span>

## <span data-ttu-id="947aa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="947aa-104">SYNTAX</span></span>

### <span data-ttu-id="947aa-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="947aa-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="947aa-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="947aa-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="947aa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="947aa-107">DESCRIPTION</span></span>
<span data-ttu-id="947aa-108">Cmdleten **Get-AzStorageAccount** hämtar ett angivet lagrings konto eller alla lagrings konton i en resurs grupp eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="947aa-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="947aa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="947aa-109">EXAMPLES</span></span>

### <span data-ttu-id="947aa-110">Exempel 1: skaffa ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="947aa-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="947aa-111">Det här kommandot hämtar det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="947aa-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="947aa-112">Exempel 2: Hämta alla lagrings konton i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="947aa-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="947aa-113">Det här kommandot får alla lagrings konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="947aa-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="947aa-114">Exempel 3: Hämta alla lagrings konton i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="947aa-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="947aa-115">Det här kommandot får alla lagrings konton i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="947aa-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="947aa-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="947aa-116">PARAMETERS</span></span>

### <span data-ttu-id="947aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="947aa-117">-DefaultProfile</span></span>
<span data-ttu-id="947aa-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="947aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="947aa-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="947aa-119">-Name</span></span>
<span data-ttu-id="947aa-120">Anger namnet på det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="947aa-120">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="947aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="947aa-122">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="947aa-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947aa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="947aa-123">CommonParameters</span></span>
<span data-ttu-id="947aa-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="947aa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="947aa-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="947aa-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="947aa-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="947aa-126">INPUTS</span></span>

### <span data-ttu-id="947aa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="947aa-127">System.String</span></span>

## <span data-ttu-id="947aa-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="947aa-128">OUTPUTS</span></span>

### <span data-ttu-id="947aa-129">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="947aa-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="947aa-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="947aa-130">NOTES</span></span>

## <span data-ttu-id="947aa-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="947aa-131">RELATED LINKS</span></span>

[<span data-ttu-id="947aa-132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="947aa-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="947aa-133">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="947aa-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="947aa-134">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="947aa-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


