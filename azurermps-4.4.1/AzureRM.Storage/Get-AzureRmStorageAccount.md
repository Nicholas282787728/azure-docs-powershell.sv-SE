---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: 07fdf5a05f5099facabb78f35c44856545d1efe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755790"
---
# <span data-ttu-id="6fdbb-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6fdbb-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="6fdbb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fdbb-102">SYNOPSIS</span></span>
<span data-ttu-id="6fdbb-103">Hämtar ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6fdbb-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fdbb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fdbb-104">SYNTAX</span></span>

### <span data-ttu-id="6fdbb-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fdbb-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6fdbb-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fdbb-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fdbb-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fdbb-107">DESCRIPTION</span></span>
<span data-ttu-id="6fdbb-108">Cmdleten **Get-AzureRmStorageAccount** hämtar ett angivet lagrings konto eller alla lagrings konton i en resurs grupp eller prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6fdbb-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="6fdbb-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fdbb-109">EXAMPLES</span></span>

### <span data-ttu-id="6fdbb-110">Exempel 1: skaffa ett angivet lagrings konto</span><span class="sxs-lookup"><span data-stu-id="6fdbb-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="6fdbb-111">Det här kommandot hämtar det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="6fdbb-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="6fdbb-112">Exempel 2: Hämta alla lagrings konton i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="6fdbb-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="6fdbb-113">Det här kommandot får alla lagrings konton i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6fdbb-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="6fdbb-114">Exempel 3: Hämta alla lagrings konton i prenumerationen</span><span class="sxs-lookup"><span data-stu-id="6fdbb-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="6fdbb-115">Det här kommandot får alla lagrings konton i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6fdbb-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="6fdbb-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fdbb-116">PARAMETERS</span></span>

### <span data-ttu-id="6fdbb-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="6fdbb-117">-Name</span></span>
<span data-ttu-id="6fdbb-118">Anger namnet på det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="6fdbb-118">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="6fdbb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fdbb-119">-ResourceGroupName</span></span>
<span data-ttu-id="6fdbb-120">Anger namnet på den resurs grupp som innehåller det lagrings konto som ska visas.</span><span class="sxs-lookup"><span data-stu-id="6fdbb-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="6fdbb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fdbb-121">-DefaultProfile</span></span>
<span data-ttu-id="6fdbb-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fdbb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fdbb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fdbb-123">CommonParameters</span></span>
<span data-ttu-id="6fdbb-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fdbb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fdbb-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fdbb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fdbb-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fdbb-126">INPUTS</span></span>

## <span data-ttu-id="6fdbb-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fdbb-127">OUTPUTS</span></span>

## <span data-ttu-id="6fdbb-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fdbb-128">NOTES</span></span>

## <span data-ttu-id="6fdbb-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fdbb-129">RELATED LINKS</span></span>

[<span data-ttu-id="6fdbb-130">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6fdbb-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="6fdbb-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6fdbb-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="6fdbb-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6fdbb-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


