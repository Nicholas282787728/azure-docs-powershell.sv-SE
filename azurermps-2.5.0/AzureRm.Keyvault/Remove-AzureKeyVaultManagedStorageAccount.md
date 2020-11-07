---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
ms.openlocfilehash: 438d36a5c9081da3124c0ef5ee03c7eb9ad8f634
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928798"
---
# <span data-ttu-id="0fa48-101">Remove-AzureKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0fa48-101">Remove-AzureKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="0fa48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0fa48-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa48-103">Tar bort ett Key valv-hanterat Azure Storage-konto och alla tillhör ande SAS-definitioner.</span><span class="sxs-lookup"><span data-stu-id="0fa48-103">Removes a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fa48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0fa48-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-AccountName] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fa48-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0fa48-105">DESCRIPTION</span></span>
<span data-ttu-id="0fa48-106">Avassocierar ett Azure Storage-konto från Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0fa48-106">Disassociates an Azure Storage Account from Key Vault.</span></span> <span data-ttu-id="0fa48-107">Detta tar inte bort ett Azure Storage-konto, men tar bort konto nycklarna från att hanteras av Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="0fa48-107">This does not remove an Azure Storage Account but removes the account keys from being managed by Azure Key Vault.</span></span> <span data-ttu-id="0fa48-108">Alla tillhör ande säkerhets associationer för hanterade nycklar för nyckelbaserad lagring tas också bort.</span><span class="sxs-lookup"><span data-stu-id="0fa48-108">All associated Key Vault managed Storage SAS definitions are also removed.</span></span>

## <span data-ttu-id="0fa48-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0fa48-109">EXAMPLES</span></span>

### <span data-ttu-id="0fa48-110">Exempel 1: ta bort ett Key valv-hanterat Azure Storage-konto och alla tillhör ande SAS-definitioner.</span><span class="sxs-lookup"><span data-stu-id="0fa48-110">Example 1: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount'
```

<span data-ttu-id="0fa48-111">Avassocierar Azure Storage-kontot ' mystorageaccount ' från nyckel valv ' The valv ' och stoppar nyckel valvet för att hantera dess nycklar.</span><span class="sxs-lookup"><span data-stu-id="0fa48-111">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="0fa48-112">Kontot ' mystorageaccount ' kommer inte att tas bort.</span><span class="sxs-lookup"><span data-stu-id="0fa48-112">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="0fa48-113">Alla säkerhets associationer för viktiga nycklar som hanteras med det här kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="0fa48-113">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

### <span data-ttu-id="0fa48-114">Exempel 2: ta bort ett Key valv-hanterat Azure Storage-konto och alla tillhör ande sa-definitioner utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0fa48-114">Example 2: Remove a Key Vault managed Azure Storage Account and all associated SAS definitions without user confirmation.</span></span>
```
PS C:\> Remove-AzureKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Force -Confirm:$False
```

<span data-ttu-id="0fa48-115">Avassocierar Azure Storage-kontot ' mystorageaccount ' från nyckel valv ' The valv ' och stoppar nyckel valvet för att hantera dess nycklar.</span><span class="sxs-lookup"><span data-stu-id="0fa48-115">Disassociates Azure Storage Account 'mystorageaccount' from Key Vault 'myvault' and stops Key Vault from managing its keys.</span></span> <span data-ttu-id="0fa48-116">Kontot ' mystorageaccount ' kommer inte att tas bort.</span><span class="sxs-lookup"><span data-stu-id="0fa48-116">The account 'mystorageaccount' will not be removed.</span></span> <span data-ttu-id="0fa48-117">Alla säkerhets associationer för viktiga nycklar som hanteras med det här kontot tas bort.</span><span class="sxs-lookup"><span data-stu-id="0fa48-117">All Key Vault managed Storage SAS definitions associated with this account will be removed.</span></span>

## <span data-ttu-id="0fa48-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0fa48-118">PARAMETERS</span></span>

### <span data-ttu-id="0fa48-119">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0fa48-119">-AccountName</span></span>
<span data-ttu-id="0fa48-120">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="0fa48-120">Key Vault managed storage account name.</span></span> <span data-ttu-id="0fa48-121">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="0fa48-121">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="0fa48-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa48-122">-DefaultProfile</span></span>
<span data-ttu-id="0fa48-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="0fa48-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0fa48-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0fa48-124">-Force</span></span>
<span data-ttu-id="0fa48-125">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0fa48-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0fa48-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fa48-126">-PassThru</span></span>
<span data-ttu-id="0fa48-127">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="0fa48-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0fa48-128">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="0fa48-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="0fa48-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0fa48-129">-VaultName</span></span>
<span data-ttu-id="0fa48-130">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="0fa48-130">Vault name.</span></span>
<span data-ttu-id="0fa48-131">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="0fa48-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0fa48-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0fa48-132">-Confirm</span></span>
<span data-ttu-id="0fa48-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0fa48-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa48-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa48-134">-WhatIf</span></span>
<span data-ttu-id="0fa48-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0fa48-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fa48-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0fa48-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa48-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa48-137">CommonParameters</span></span>
<span data-ttu-id="0fa48-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa48-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa48-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fa48-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa48-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0fa48-140">INPUTS</span></span>

### <span data-ttu-id="0fa48-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0fa48-141">System.String</span></span>

## <span data-ttu-id="0fa48-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0fa48-142">OUTPUTS</span></span>

### <span data-ttu-id="0fa48-143">Microsoft. Azure. commands. valv. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0fa48-143">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="0fa48-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0fa48-144">NOTES</span></span>

## <span data-ttu-id="0fa48-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0fa48-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

