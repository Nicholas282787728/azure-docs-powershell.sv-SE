---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: 98c4cca6b2de508ca48da4ccbc5cf9f9a31eaa0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922678"
---
# <span data-ttu-id="548d8-101">Remove-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="548d8-101">Remove-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="548d8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="548d8-102">SYNOPSIS</span></span>
<span data-ttu-id="548d8-103">Tar bort en Key valv Managed-definitioner för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="548d8-103">Removes a Key Vault managed Azure Storage SAS definitions.</span></span>

## <span data-ttu-id="548d8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="548d8-104">SYNTAX</span></span>

```
Remove-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548d8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="548d8-105">DESCRIPTION</span></span>
<span data-ttu-id="548d8-106">Tar bort en Key valv Managed-definitioner för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="548d8-106">Removes a Key Vault managed Azure Storage SAS definitions.</span></span> <span data-ttu-id="548d8-107">Detta tar också bort hemligheten som används för att hämta SAS-token per denna säkerhets Association.</span><span class="sxs-lookup"><span data-stu-id="548d8-107">This also removes the secret used to get the SAS token per this SAS definition.</span></span>

## <span data-ttu-id="548d8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="548d8-108">EXAMPLES</span></span>

### <span data-ttu-id="548d8-109">Exempel 1: ta bort en Key valv Managed definition för Azure-lagring.</span><span class="sxs-lookup"><span data-stu-id="548d8-109">Example 1: Remove a Key Vault managed Azure Storage SAS definition.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef'
```

<span data-ttu-id="548d8-110">Tar bort säkerhets associationer för Managed Storage mysasdef associerat med kontot ' mystorageaccount ' i valv för valvet.</span><span class="sxs-lookup"><span data-stu-id="548d8-110">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

### <span data-ttu-id="548d8-111">Exempel 2: ta bort en Key valv Managed definition av Azure-lagring utan bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="548d8-111">Example 2: Remove a Key Vault managed Azure Storage SAS definition without user confirmation.</span></span>
```
PS C:\> Remove-AzKeyVaultManagedStorageAccount -VaultName 'myvault' -AccountName 'mystorageaccount' -Name 'mysasdef' -Force -Confirm:$False
```

<span data-ttu-id="548d8-112">Tar bort säkerhets associationer för Managed Storage mysasdef associerat med kontot ' mystorageaccount ' i valv för valvet.</span><span class="sxs-lookup"><span data-stu-id="548d8-112">Removes a Key Vault managed Storage SAS definition 'mysasdef' associated with the account 'mystorageaccount' in vault 'myvault'.</span></span>

## <span data-ttu-id="548d8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="548d8-113">PARAMETERS</span></span>

### <span data-ttu-id="548d8-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="548d8-114">-AccountName</span></span>
<span data-ttu-id="548d8-115">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="548d8-115">Storage account name.</span></span>
<span data-ttu-id="548d8-116">Cmdlet konstruerar FQDN för ett hanterat lagrings konto namn från ett valv namn, valt miljö-och lagrings konto namn.</span><span class="sxs-lookup"><span data-stu-id="548d8-116">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548d8-117">-DefaultProfile</span></span>
<span data-ttu-id="548d8-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="548d8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="548d8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="548d8-119">-Force</span></span>
<span data-ttu-id="548d8-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="548d8-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="548d8-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="548d8-121">-Name</span></span>
<span data-ttu-id="548d8-122">Namn på lagrings-sa.</span><span class="sxs-lookup"><span data-stu-id="548d8-122">Storage sas definition name.</span></span>
<span data-ttu-id="548d8-123">Cmdlet konstruerar FQDN-namnet på en lagrings-säkerhets Association från ett valv namn, för närvarande valda miljö-, lagrings konto namn och SAS-namn.</span><span class="sxs-lookup"><span data-stu-id="548d8-123">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="548d8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="548d8-124">-PassThru</span></span>
<span data-ttu-id="548d8-125">Cmdlet returnerar inte ett objekt som standard.</span><span class="sxs-lookup"><span data-stu-id="548d8-125">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="548d8-126">Om denna växel anges returnerar cmdlet det hanterade lagrings konto som har tagits bort.</span><span class="sxs-lookup"><span data-stu-id="548d8-126">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="548d8-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="548d8-127">-VaultName</span></span>
<span data-ttu-id="548d8-128">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="548d8-128">Vault name.</span></span>
<span data-ttu-id="548d8-129">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="548d8-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="548d8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="548d8-130">-Confirm</span></span>
<span data-ttu-id="548d8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="548d8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548d8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548d8-132">-WhatIf</span></span>
<span data-ttu-id="548d8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="548d8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548d8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="548d8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548d8-135">CommonParameters</span></span>
<span data-ttu-id="548d8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548d8-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548d8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548d8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="548d8-138">INPUTS</span></span>

### <span data-ttu-id="548d8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="548d8-139">System.String</span></span>

## <span data-ttu-id="548d8-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="548d8-140">OUTPUTS</span></span>

### <span data-ttu-id="548d8-141">Microsoft. Azure. commands. valv. Models. ManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="548d8-141">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="548d8-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="548d8-142">NOTES</span></span>

## <span data-ttu-id="548d8-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="548d8-143">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

