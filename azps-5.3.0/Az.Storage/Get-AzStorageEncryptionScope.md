---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageencryptionscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageEncryptionScope.md
ms.openlocfilehash: cdc2f8b1742625feb042865a9b75e2c495d7aac2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522171"
---
# <span data-ttu-id="4754f-101">Get-AzStorageEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4754f-101">Get-AzStorageEncryptionScope</span></span>

## <span data-ttu-id="4754f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4754f-102">SYNOPSIS</span></span>
<span data-ttu-id="4754f-103">Hämta eller lista krypterings omfattningar från ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4754f-103">Get or list encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="4754f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4754f-104">SYNTAX</span></span>

### <span data-ttu-id="4754f-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="4754f-105">AccountName (Default)</span></span>
```
Get-AzStorageEncryptionScope [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EncryptionScopeName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4754f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4754f-106">AccountObject</span></span>
```
Get-AzStorageEncryptionScope -StorageAccount <PSStorageAccount> [-EncryptionScopeName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4754f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4754f-107">DESCRIPTION</span></span>
<span data-ttu-id="4754f-108">Cmdleten **Get-AzStorageEncryptionScope** hämtar eller visar krypterings områden från ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4754f-108">The **Get-AzStorageEncryptionScope** cmdlet gets or lists encryption scopes from a Storage account.</span></span>

## <span data-ttu-id="4754f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4754f-109">EXAMPLES</span></span>

### <span data-ttu-id="4754f-110">Exempel 1: skaffa en enda krypterings omfattning</span><span class="sxs-lookup"><span data-stu-id="4754f-110">Example 1: Get a single encryption scope</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EncryptionScopeName $scopename


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
```

<span data-ttu-id="4754f-111">Det här kommandot får en enda krypterings omfattning.</span><span class="sxs-lookup"><span data-stu-id="4754f-111">This command gets a single encryption scope.</span></span>

### <span data-ttu-id="4754f-112">Exempel 2: lista alla krypterings områden för ett lagrings konto</span><span class="sxs-lookup"><span data-stu-id="4754f-112">Example 2: List all encryption scopes of a Storage account</span></span>
```
PS C:\> Get-AzStorageEncryptionScope -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" 


   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name      State    Source             KeyVaultKeyUri                                         
----      -----    ------             --------------                                         
testscope Disabled Microsoft.Keyvault https://keyvalutname.vault.azure.net:443/keys/keyname
scope2    Enabled  Microsoft.Storage
```

<span data-ttu-id="4754f-113">Det här kommandot listar alla krypterings områden för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4754f-113">This command lists all encryption scopes of a Storage account.</span></span>

## <span data-ttu-id="4754f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4754f-114">PARAMETERS</span></span>

### <span data-ttu-id="4754f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4754f-115">-DefaultProfile</span></span>
<span data-ttu-id="4754f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4754f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4754f-117">-EncryptionScopeName</span><span class="sxs-lookup"><span data-stu-id="4754f-117">-EncryptionScopeName</span></span>
<span data-ttu-id="4754f-118">Namn på Azure-EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4754f-118">Azure Storage EncryptionScope name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4754f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4754f-119">-ResourceGroupName</span></span>
<span data-ttu-id="4754f-120">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="4754f-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4754f-121">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4754f-121">-StorageAccount</span></span>
<span data-ttu-id="4754f-122">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="4754f-122">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4754f-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4754f-123">-StorageAccountName</span></span>
<span data-ttu-id="4754f-124">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="4754f-124">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4754f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4754f-125">CommonParameters</span></span>
<span data-ttu-id="4754f-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4754f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4754f-127">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4754f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4754f-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4754f-128">INPUTS</span></span>

### <span data-ttu-id="4754f-129">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4754f-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4754f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4754f-130">OUTPUTS</span></span>

### <span data-ttu-id="4754f-131">Microsoft. Azure. commands. Management. Storage. Models. PSEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="4754f-131">Microsoft.Azure.Commands.Management.Storage.Models.PSEncryptionScope</span></span>

## <span data-ttu-id="4754f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4754f-132">NOTES</span></span>

## <span data-ttu-id="4754f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4754f-133">RELATED LINKS</span></span>
