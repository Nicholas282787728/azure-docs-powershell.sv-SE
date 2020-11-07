---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 26bf7b91b330032e05f96f425cb21908fc3df55d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916198"
---
# <span data-ttu-id="6ef50-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="6ef50-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="6ef50-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6ef50-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef50-103">Återställer en borttagen hemlighet i ett nyckel valv till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="6ef50-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="6ef50-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6ef50-104">SYNTAX</span></span>

### <span data-ttu-id="6ef50-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="6ef50-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ef50-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6ef50-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ef50-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6ef50-107">DESCRIPTION</span></span>
<span data-ttu-id="6ef50-108">Cmdleten **Undo-AzKeyVaultSecretRemoval** återställer en tidigare borttagen hemlighet.</span><span class="sxs-lookup"><span data-stu-id="6ef50-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="6ef50-109">Den återställda hemligheten aktive ras och kan användas för alla vanliga hemliga åtgärder.</span><span class="sxs-lookup"><span data-stu-id="6ef50-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="6ef50-110">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6ef50-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="6ef50-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6ef50-111">EXAMPLES</span></span>

### <span data-ttu-id="6ef50-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6ef50-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

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

<span data-ttu-id="6ef50-113">Det här kommandot återställer hemligheten "hemlig" som tidigare har tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="6ef50-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="6ef50-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6ef50-114">PARAMETERS</span></span>

### <span data-ttu-id="6ef50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef50-115">-DefaultProfile</span></span>
<span data-ttu-id="6ef50-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6ef50-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ef50-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ef50-117">-InputObject</span></span>
<span data-ttu-id="6ef50-118">Borttaget hemligt objekt</span><span class="sxs-lookup"><span data-stu-id="6ef50-118">Deleted secret object</span></span>

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

### <span data-ttu-id="6ef50-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="6ef50-119">-Name</span></span>
<span data-ttu-id="6ef50-120">Hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="6ef50-120">Secret name.</span></span>
<span data-ttu-id="6ef50-121">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="6ef50-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="6ef50-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6ef50-122">-VaultName</span></span>
<span data-ttu-id="6ef50-123">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="6ef50-123">Vault name.</span></span>
<span data-ttu-id="6ef50-124">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="6ef50-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="6ef50-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6ef50-125">-Confirm</span></span>
<span data-ttu-id="6ef50-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6ef50-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ef50-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ef50-127">-WhatIf</span></span>
<span data-ttu-id="6ef50-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6ef50-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ef50-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6ef50-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ef50-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef50-130">CommonParameters</span></span>
<span data-ttu-id="6ef50-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ef50-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef50-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ef50-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef50-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6ef50-133">INPUTS</span></span>

### <span data-ttu-id="6ef50-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6ef50-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="6ef50-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6ef50-135">OUTPUTS</span></span>

### <span data-ttu-id="6ef50-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6ef50-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="6ef50-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6ef50-137">NOTES</span></span>

## <span data-ttu-id="6ef50-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6ef50-138">RELATED LINKS</span></span>

[<span data-ttu-id="6ef50-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6ef50-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="6ef50-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6ef50-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="6ef50-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6ef50-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
