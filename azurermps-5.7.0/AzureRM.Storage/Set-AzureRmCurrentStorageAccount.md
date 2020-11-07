---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermcurrentstorageaccount
schema: 2.0.0
ms.openlocfilehash: 6a7ef50e6e95a30140549343d14d4a75ad340cbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756765"
---
# <span data-ttu-id="955a8-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="955a8-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="955a8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="955a8-102">SYNOPSIS</span></span>
<span data-ttu-id="955a8-103">Ändrar det aktuella lagrings kontot för den angivna prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="955a8-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="955a8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="955a8-104">SYNTAX</span></span>

### <span data-ttu-id="955a8-105">UsingResourceGroupAndNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="955a8-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="955a8-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="955a8-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="955a8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="955a8-107">DESCRIPTION</span></span>
<span data-ttu-id="955a8-108">Cmdleten **set-AzureRmCurrentStorageAccount** ändrar det aktuella Azure Storage-kontot för det angivna Azure-abonnemanget i Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="955a8-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="955a8-109">Det aktuella lagrings kontot används som standard när du öppnar lagring utan att ange ett lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="955a8-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="955a8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="955a8-110">EXAMPLES</span></span>

### <span data-ttu-id="955a8-111">Exempel 1: Ange det aktuella lagrings kontot</span><span class="sxs-lookup"><span data-stu-id="955a8-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="955a8-112">Det här kommandot anger standard lagrings kontot för den angivna prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="955a8-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="955a8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="955a8-113">PARAMETERS</span></span>

### <span data-ttu-id="955a8-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="955a8-114">-Context</span></span>
<span data-ttu-id="955a8-115">Anger ett **AzureStorageContext** -objekt för det aktuella lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="955a8-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="955a8-116">Använd New-AzureStorageContext cmdlet för att få ett lagrings kontext objekt.</span><span class="sxs-lookup"><span data-stu-id="955a8-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: UsingStorageContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="955a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955a8-117">-DefaultProfile</span></span>
<span data-ttu-id="955a8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="955a8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="955a8-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="955a8-119">-Name</span></span>
<span data-ttu-id="955a8-120">Anger namnet på det lagrings konto som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="955a8-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="955a8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="955a8-121">-ResourceGroupName</span></span>
<span data-ttu-id="955a8-122">Anger den resurs grupp som innehåller det lagrings konto som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="955a8-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="955a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955a8-123">CommonParameters</span></span>
<span data-ttu-id="955a8-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="955a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955a8-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="955a8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955a8-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="955a8-126">INPUTS</span></span>

### <span data-ttu-id="955a8-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="955a8-127">IStorageContext</span></span>
<span data-ttu-id="955a8-128">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="955a8-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="955a8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="955a8-129">OUTPUTS</span></span>

### <span data-ttu-id="955a8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="955a8-130">System.String</span></span>

## <span data-ttu-id="955a8-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="955a8-131">NOTES</span></span>

## <span data-ttu-id="955a8-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="955a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="955a8-133">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="955a8-133">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


