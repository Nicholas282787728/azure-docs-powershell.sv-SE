---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: c57f8a7ce6b4f7275e724c777c2e6dfd54a680ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090784"
---
# <span data-ttu-id="09f89-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09f89-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="09f89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09f89-102">SYNOPSIS</span></span>
<span data-ttu-id="09f89-103">Ändrar det aktuella lagrings kontot för den angivna prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="09f89-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="09f89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09f89-104">SYNTAX</span></span>

### <span data-ttu-id="09f89-105">UsingResourceGroupAndNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="09f89-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09f89-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="09f89-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09f89-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09f89-107">DESCRIPTION</span></span>
<span data-ttu-id="09f89-108">Cmdleten **set-AzCurrentStorageAccount** ändrar det aktuella Azure Storage-kontot för det angivna Azure-abonnemanget i Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09f89-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="09f89-109">Det aktuella lagrings kontot används som standard när du öppnar lagring utan att ange ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="09f89-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="09f89-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09f89-110">EXAMPLES</span></span>

### <span data-ttu-id="09f89-111">Exempel 1: Ange det aktuella lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="09f89-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="09f89-112">Det här kommandot anger standard lagrings kontot för den angivna prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="09f89-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="09f89-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09f89-113">PARAMETERS</span></span>

### <span data-ttu-id="09f89-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="09f89-114">-Context</span></span>
<span data-ttu-id="09f89-115">Anger ett **AzureStorageContext** -objekt för det aktuella lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="09f89-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="09f89-116">Använd New-AzStorageContext cmdlet för att få ett lagrings kontext objekt.</span><span class="sxs-lookup"><span data-stu-id="09f89-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09f89-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f89-117">-DefaultProfile</span></span>
<span data-ttu-id="09f89-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09f89-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f89-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="09f89-119">-Name</span></span>
<span data-ttu-id="09f89-120">Anger namnet på det lagrings konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="09f89-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f89-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f89-121">-ResourceGroupName</span></span>
<span data-ttu-id="09f89-122">Anger den resurs grupp som innehåller det lagrings konto som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="09f89-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09f89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f89-123">CommonParameters</span></span>
<span data-ttu-id="09f89-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f89-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09f89-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f89-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09f89-126">INPUTS</span></span>

### <span data-ttu-id="09f89-127">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="09f89-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="09f89-128">System. String</span><span class="sxs-lookup"><span data-stu-id="09f89-128">System.String</span></span>

## <span data-ttu-id="09f89-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09f89-129">OUTPUTS</span></span>

### <span data-ttu-id="09f89-130">System. String</span><span class="sxs-lookup"><span data-stu-id="09f89-130">System.String</span></span>

## <span data-ttu-id="09f89-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09f89-131">NOTES</span></span>

## <span data-ttu-id="09f89-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09f89-132">RELATED LINKS</span></span>

[<span data-ttu-id="09f89-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09f89-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)

