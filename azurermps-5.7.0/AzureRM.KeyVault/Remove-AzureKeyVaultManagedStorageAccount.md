---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c422975af622fe54602224b0c311ea8e738f838f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755751"
---
# <span data-ttu-id="3d030-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d030-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="3d030-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d030-102">SYNOPSIS</span></span>
<span data-ttu-id="3d030-103">Tar bort ett Key valv-hanterat Azure Storage-konto och alla tillhör ande SAS-definitioner.</span><span class="sxs-lookup"><span data-stu-id="3d030-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d030-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d030-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d030-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d030-105">DESCRIPTION</span></span>
<span data-ttu-id="3d030-106">Avassocierar ett Azure Storage-konto från Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3d030-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="3d030-107">Detta tar inte bort ett Azure Storage-konto, men tar bort konto nycklarna från att hanteras av Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="3d030-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="3d030-108">Alla tillhör ande säkerhets associationer för hanterade nycklar för nyckelbaserad lagring tas också bort.</span><span class="sxs-lookup"><span data-stu-id="3d030-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="3d030-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d030-109">EXAMPLES</span></span>

### <span data-ttu-id="3d030-110">Exempel 1: ta bort ett Key valv-hanterat Azure Storage-konto och alla tillhör ande SAS-definitioner.</span><span class="sxs-lookup"><span data-stu-id="3d030-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="3d030-111">Avassocierar Azure Storage-kontot ' mystorageaccount ' från nyckel valv ' The valv ' och stoppar nyckel valvet för att hantera dess nycklar.</span><span class="sxs-lookup"><span data-stu-id="3d030-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="3d030-112">Kontot ' mystorageaccount ' kommer inte att tas bort.</span><span class="sxs-lookup"><span data-stu-id="3d030-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="3d030-113">Alla säkerhets associationer för viktiga nycklar som hanteras med det här kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="3d030-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="3d030-114">Exempel 2: ta bort ett Key valv-hanterat Azure Storage-konto och alla tillhör ande sa-definitioner utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3d030-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="3d030-115">Avassocierar Azure Storage-kontot ' mystorageaccount ' från nyckel valv ' The valv ' och stoppar nyckel valvet för att hantera dess nycklar.</span><span class="sxs-lookup"><span data-stu-id="3d030-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="3d030-116">Kontot ' mystorageaccount ' kommer inte att tas bort.</span><span class="sxs-lookup"><span data-stu-id="3d030-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="3d030-117">Alla säkerhets associationer för viktiga nycklar som hanteras med det här kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="3d030-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="3d030-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d030-118">PARAMETERS</span></span>

### <span data-ttu-id="3d030-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3d030-119">-AccountName</span></span>
<span data-ttu-id="3d030-120">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="3d030-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="3d030-121">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="3d030-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d030-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d030-122">-DefaultProfile</span></span>
<span data-ttu-id="3d030-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3d030-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d030-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3d030-124">-Force</span></span>
<span data-ttu-id="3d030-125">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3d030-125">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d030-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d030-126">-PassThru</span></span>
<span data-ttu-id="3d030-127">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="3d030-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3d030-128">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="3d030-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d030-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3d030-129">-VaultName</span></span>
<span data-ttu-id="3d030-130">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="3d030-130">Vault name.</span></span>
<span data-ttu-id="3d030-131">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="3d030-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d030-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d030-132">-Confirm</span></span>
<span data-ttu-id="3d030-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d030-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d030-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d030-134">-WhatIf</span></span>
<span data-ttu-id="3d030-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d030-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d030-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d030-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d030-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d030-137">CommonParameters</span></span>
<span data-ttu-id="3d030-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d030-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d030-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d030-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d030-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d030-140">INPUTS</span></span>

### <span data-ttu-id="3d030-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3d030-141">System.String</span></span>

## <span data-ttu-id="3d030-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d030-142">OUTPUTS</span></span>

### <span data-ttu-id="3d030-143">Microsoft. Azure. commands. valv. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d030-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="3d030-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d030-144">NOTES</span></span>

## <span data-ttu-id="3d030-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d030-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

