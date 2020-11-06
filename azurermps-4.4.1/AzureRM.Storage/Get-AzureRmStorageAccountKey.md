---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: d12be29507f581f3e9a8d0de86d8a571a305908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576680"
---
# <span data-ttu-id="29183-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="29183-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="29183-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29183-102">SYNOPSIS</span></span>
<span data-ttu-id="29183-103">Hämtar åtkomst nycklar för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="29183-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29183-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29183-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29183-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29183-105">DESCRIPTION</span></span>
<span data-ttu-id="29183-106">Cmdleten **Get-AzureRmStorageAccountKey** hämtar åtkomst nycklar för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="29183-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="29183-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29183-107">EXAMPLES</span></span>

### <span data-ttu-id="29183-108">Exempel 1: Hämta snabb tangenterna för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="29183-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="29183-109">Det här kommandot får nycklarna för det angivna Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="29183-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="29183-110">Exempel 2: Hämta en specifik åtkomst för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="29183-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="29183-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29183-111">PARAMETERS</span></span>

### <span data-ttu-id="29183-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="29183-112">-Name</span></span>
<span data-ttu-id="29183-113">Anger namnet på det lagrings konto som den här cmdleten får nycklar för.</span><span class="sxs-lookup"><span data-stu-id="29183-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29183-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29183-114">-ResourceGroupName</span></span>
<span data-ttu-id="29183-115">Anger namnet på den resurs grupp som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="29183-115">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29183-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29183-116">-DefaultProfile</span></span>
<span data-ttu-id="29183-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="29183-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29183-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29183-118">CommonParameters</span></span>
<span data-ttu-id="29183-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29183-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29183-120">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29183-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29183-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29183-121">INPUTS</span></span>

## <span data-ttu-id="29183-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29183-122">OUTPUTS</span></span>

## <span data-ttu-id="29183-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29183-123">NOTES</span></span>

## <span data-ttu-id="29183-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29183-124">RELATED LINKS</span></span>

[<span data-ttu-id="29183-125">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="29183-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


