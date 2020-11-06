---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: ecc22deb6be4f8fe85b66454091f6bfbd01d3a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576953"
---
# <span data-ttu-id="e6ec0-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="e6ec0-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="e6ec0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e6ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="e6ec0-103">Återställer en borttagen hemlighet i ett nyckel valv till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6ec0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e6ec0-104">SYNTAX</span></span>

### <span data-ttu-id="e6ec0-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="e6ec0-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6ec0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e6ec0-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6ec0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e6ec0-107">DESCRIPTION</span></span>
<span data-ttu-id="e6ec0-108">Cmdleten **Undo-AzureKeyVaultSecretRemoval** återställer en tidigare borttagen hemlighet.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="e6ec0-109">Den återställda hemligheten aktive ras och kan användas för alla vanliga hemliga åtgärder.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="e6ec0-110">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="e6ec0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e6ec0-111">EXAMPLES</span></span>

### <span data-ttu-id="e6ec0-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e6ec0-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="e6ec0-113">Det här kommandot återställer hemligheten "hemlig" som tidigare har tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="e6ec0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e6ec0-114">PARAMETERS</span></span>

### <span data-ttu-id="e6ec0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6ec0-115">-DefaultProfile</span></span>
<span data-ttu-id="e6ec0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e6ec0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6ec0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6ec0-117">-InputObject</span></span>
<span data-ttu-id="e6ec0-118">Borttaget hemligt objekt</span><span class="sxs-lookup"><span data-stu-id="e6ec0-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6ec0-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e6ec0-119">-Name</span></span>
<span data-ttu-id="e6ec0-120">Hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-120">Secret name.</span></span>
<span data-ttu-id="e6ec0-121">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ec0-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e6ec0-122">-VaultName</span></span>
<span data-ttu-id="e6ec0-123">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-123">Vault name.</span></span>
<span data-ttu-id="e6ec0-124">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6ec0-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e6ec0-125">-Confirm</span></span>
<span data-ttu-id="e6ec0-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6ec0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6ec0-127">-WhatIf</span></span>
<span data-ttu-id="e6ec0-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6ec0-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6ec0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6ec0-130">CommonParameters</span></span>
<span data-ttu-id="e6ec0-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6ec0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6ec0-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6ec0-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6ec0-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e6ec0-133">INPUTS</span></span>

### <span data-ttu-id="e6ec0-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="e6ec0-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="e6ec0-135">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e6ec0-135">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e6ec0-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e6ec0-136">OUTPUTS</span></span>

### <span data-ttu-id="e6ec0-137">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e6ec0-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="e6ec0-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e6ec0-138">NOTES</span></span>

## <span data-ttu-id="e6ec0-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e6ec0-139">RELATED LINKS</span></span>

[<span data-ttu-id="e6ec0-140">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e6ec0-140">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="e6ec0-141">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e6ec0-141">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="e6ec0-142">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e6ec0-142">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
