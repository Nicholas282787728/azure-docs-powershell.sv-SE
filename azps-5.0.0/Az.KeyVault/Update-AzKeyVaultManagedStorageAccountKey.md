---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: b603cff68d2343a683718ca53e900aa5b667dc14
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273421"
---
# <span data-ttu-id="ff33d-101">Update-AzKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff33d-101">Update-AzKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="ff33d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ff33d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff33d-103">Återskapar den angivna nyckeln för ett Azure Storage-konto med Key valv.</span><span class="sxs-lookup"><span data-stu-id="ff33d-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ff33d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ff33d-104">SYNTAX</span></span>

### <span data-ttu-id="ff33d-105">ByDefinitionName (standard)</span><span class="sxs-lookup"><span data-stu-id="ff33d-105">ByDefinitionName (Default)</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff33d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ff33d-106">ByInputObject</span></span>
```
Update-AzKeyVaultManagedStorageAccountKey [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-KeyName] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff33d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ff33d-107">DESCRIPTION</span></span>
<span data-ttu-id="ff33d-108">Återskapar den angivna nyckeln för ett Azure Storage-konto för Key valv som hanteras och anger nyckeln som den aktiva nyckeln.</span><span class="sxs-lookup"><span data-stu-id="ff33d-108">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="ff33d-109">Key valv proxyservrar samtalet till Azure Resource Manager för att återskapa nyckeln.</span><span class="sxs-lookup"><span data-stu-id="ff33d-109">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="ff33d-110">Den som anropar måste Posses behörigheter för att kunna återskapa nycklar på angivet Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="ff33d-110">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="ff33d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ff33d-111">EXAMPLES</span></span>

### <span data-ttu-id="ff33d-112">Exempel 1: återskapa en nyckeln</span><span class="sxs-lookup"><span data-stu-id="ff33d-112">Example 1: Regenerate a key</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'

Id                  : https://myvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : myvault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="ff33d-113">Återskapar ' KEY1 ' för Account ' mystorageaccount ' och anger ' KEY1 ' som aktivt för det Key valv Managed Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="ff33d-113">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="ff33d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ff33d-114">PARAMETERS</span></span>

### <span data-ttu-id="ff33d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ff33d-115">-AccountName</span></span>
<span data-ttu-id="ff33d-116">Namn på hanterat lagrings konto för viktiga valv.</span><span class="sxs-lookup"><span data-stu-id="ff33d-116">Key Vault managed storage account name.</span></span> <span data-ttu-id="ff33d-117">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från valv namn, valt miljö-och manged.</span><span class="sxs-lookup"><span data-stu-id="ff33d-117">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff33d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff33d-118">-DefaultProfile</span></span>
<span data-ttu-id="ff33d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ff33d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff33d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ff33d-120">-Force</span></span>
<span data-ttu-id="ff33d-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ff33d-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ff33d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff33d-122">-InputObject</span></span>
<span data-ttu-id="ff33d-123">ManagedStorageAccount-objekt.</span><span class="sxs-lookup"><span data-stu-id="ff33d-123">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff33d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="ff33d-124">-KeyName</span></span>
<span data-ttu-id="ff33d-125">Namn på lagrings konto nyckeln som ska återskapas och aktive ras.</span><span class="sxs-lookup"><span data-stu-id="ff33d-125">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff33d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff33d-126">-PassThru</span></span>
<span data-ttu-id="ff33d-127">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="ff33d-127">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ff33d-128">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="ff33d-128">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="ff33d-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ff33d-129">-VaultName</span></span>
<span data-ttu-id="ff33d-130">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="ff33d-130">Vault name.</span></span>
<span data-ttu-id="ff33d-131">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="ff33d-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefinitionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff33d-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ff33d-132">-Confirm</span></span>
<span data-ttu-id="ff33d-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ff33d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff33d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff33d-134">-WhatIf</span></span>
<span data-ttu-id="ff33d-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ff33d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff33d-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ff33d-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff33d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff33d-137">CommonParameters</span></span>
<span data-ttu-id="ff33d-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff33d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff33d-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff33d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff33d-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ff33d-140">INPUTS</span></span>

### <span data-ttu-id="ff33d-141">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ff33d-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="ff33d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ff33d-142">OUTPUTS</span></span>

### <span data-ttu-id="ff33d-143">Microsoft. Azure. commands. valv. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff33d-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="ff33d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ff33d-144">NOTES</span></span>

## <span data-ttu-id="ff33d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ff33d-145">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)
