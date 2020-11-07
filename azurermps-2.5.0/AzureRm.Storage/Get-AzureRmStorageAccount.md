---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: dafceede3c3732af423052d33ba125c4ad292d20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929586"
---
# <span data-ttu-id="95edd-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95edd-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="95edd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95edd-102">SYNOPSIS</span></span>
<span data-ttu-id="95edd-103">Hämtar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="95edd-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95edd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95edd-104">SYNTAX</span></span>

### <span data-ttu-id="95edd-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="95edd-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95edd-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95edd-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95edd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95edd-107">DESCRIPTION</span></span>
<span data-ttu-id="95edd-108">Cmdleten **Get-AzureRmStorageAccount** hämtar ett angivet lagrings konto eller alla lagrings konton i en resurs grupp eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="95edd-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="95edd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95edd-109">EXAMPLES</span></span>

### <span data-ttu-id="95edd-110">Exempel 1: skaffa ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="95edd-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="95edd-111">Det här kommandot hämtar det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="95edd-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="95edd-112">Exempel 2: Hämta alla lagrings konton i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="95edd-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="95edd-113">Det här kommandot får alla lagrings konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="95edd-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="95edd-114">Exempel 3: Hämta alla lagrings konton i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="95edd-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="95edd-115">Det här kommandot får alla lagrings konton i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="95edd-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="95edd-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95edd-116">PARAMETERS</span></span>

### <span data-ttu-id="95edd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95edd-117">-DefaultProfile</span></span>
<span data-ttu-id="95edd-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95edd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95edd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="95edd-119">-Name</span></span>
<span data-ttu-id="95edd-120">Anger namnet på det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="95edd-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="95edd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95edd-121">-ResourceGroupName</span></span>
<span data-ttu-id="95edd-122">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="95edd-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="95edd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95edd-123">CommonParameters</span></span>
<span data-ttu-id="95edd-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95edd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95edd-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95edd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95edd-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95edd-126">INPUTS</span></span>

### <span data-ttu-id="95edd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="95edd-127">System.String</span></span>

## <span data-ttu-id="95edd-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95edd-128">OUTPUTS</span></span>

### <span data-ttu-id="95edd-129">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95edd-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="95edd-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95edd-130">NOTES</span></span>

## <span data-ttu-id="95edd-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95edd-131">RELATED LINKS</span></span>

[<span data-ttu-id="95edd-132">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95edd-132">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="95edd-133">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95edd-133">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="95edd-134">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="95edd-134">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


