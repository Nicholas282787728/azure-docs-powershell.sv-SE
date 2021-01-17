---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388917"
---
# <span data-ttu-id="5d94b-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5d94b-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="5d94b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d94b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d94b-103">Hämtar åtkomst nycklar för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="5d94b-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="5d94b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d94b-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d94b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d94b-105">DESCRIPTION</span></span>
<span data-ttu-id="5d94b-106">Cmdleten **Get-AzStorageAccountKey** hämtar åtkomst nycklar för ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="5d94b-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="5d94b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d94b-107">EXAMPLES</span></span>

### <span data-ttu-id="5d94b-108">Exempel 1: Hämta snabb tangenterna för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5d94b-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="5d94b-109">Det här kommandot får nycklarna för det angivna Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="5d94b-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="5d94b-110">Exempel 2: Hämta en specifik åtkomst för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="5d94b-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="5d94b-111">Exempel 3: listar åtkomst nycklar för ett lagrings konto, inklusive Kerberos-nycklarna (om Active Directory är aktiverat)</span><span class="sxs-lookup"><span data-stu-id="5d94b-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="5d94b-112">Det här kommandot får nycklarna för det angivna Azure Storage-kontot.</span><span class="sxs-lookup"><span data-stu-id="5d94b-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="5d94b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d94b-113">PARAMETERS</span></span>

### <span data-ttu-id="5d94b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d94b-114">-DefaultProfile</span></span>
<span data-ttu-id="5d94b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5d94b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d94b-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="5d94b-116">-ListKerbKey</span></span>
<span data-ttu-id="5d94b-117">Visar de Kerberos-nycklar (om Active Directory är aktiverat) för det angivna lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5d94b-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="5d94b-118">Kerberos-nycklar genereras per lagrings konto för identitetsautentisering med Azure-filer antingen med Azure Active Directory Domain Service (Azure AD DS) eller Active Directory Domain Service (AD DS).</span><span class="sxs-lookup"><span data-stu-id="5d94b-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="5d94b-119">Den används som lösen ord för den identitet som är registrerad i domän tjänsten som representerar lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5d94b-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="5d94b-120">Kerberos-nycklar ger inte åtkomst behörighet för att utföra en kontroll eller data plan som läser eller skriver till lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5d94b-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d94b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d94b-121">-Name</span></span>
<span data-ttu-id="5d94b-122">Anger namnet på det lagrings konto som den här cmdleten får nycklar för.</span><span class="sxs-lookup"><span data-stu-id="5d94b-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="5d94b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d94b-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d94b-124">Anger namnet på den resurs grupp som innehåller lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="5d94b-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="5d94b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d94b-125">CommonParameters</span></span>
<span data-ttu-id="5d94b-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d94b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d94b-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d94b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d94b-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d94b-128">INPUTS</span></span>

### <span data-ttu-id="5d94b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5d94b-129">System.String</span></span>

## <span data-ttu-id="5d94b-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d94b-130">OUTPUTS</span></span>

### <span data-ttu-id="5d94b-131">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5d94b-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="5d94b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d94b-132">NOTES</span></span>

## <span data-ttu-id="5d94b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d94b-133">RELATED LINKS</span></span>

[<span data-ttu-id="5d94b-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5d94b-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


