---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: d6637b8c180dd2ef25bdba5326f0a42a364bc8ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394488"
---
# <span data-ttu-id="ccd30-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ccd30-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="ccd30-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ccd30-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd30-103">Återställer en borttagen Key i ett nyckelord till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="ccd30-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="ccd30-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ccd30-104">SYNTAX</span></span>

### <span data-ttu-id="ccd30-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="ccd30-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccd30-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="ccd30-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccd30-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ccd30-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccd30-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ccd30-108">DESCRIPTION</span></span>
<span data-ttu-id="ccd30-109">Med cmdleten **Undo-AzKeyVaultKeyRemoval** återställs en tidigare borttagen.</span><span class="sxs-lookup"><span data-stu-id="ccd30-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="ccd30-110">Den återställda knappen aktive ras och kan användas för alla vanliga viktiga operationer.</span><span class="sxs-lookup"><span data-stu-id="ccd30-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="ccd30-111">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="ccd30-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ccd30-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ccd30-112">EXAMPLES</span></span>

### <span data-ttu-id="ccd30-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ccd30-113">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="ccd30-114">Det här kommandot återställer den MyKey som du har tagit bort, i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="ccd30-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ccd30-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ccd30-115">PARAMETERS</span></span>

### <span data-ttu-id="ccd30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd30-116">-DefaultProfile</span></span>
<span data-ttu-id="ccd30-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ccd30-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccd30-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="ccd30-118">-HsmName</span></span>
<span data-ttu-id="ccd30-119">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="ccd30-119">HSM name.</span></span> <span data-ttu-id="ccd30-120">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="ccd30-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccd30-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccd30-121">-InputObject</span></span>
<span data-ttu-id="ccd30-122">Borttaget nyckeltal</span><span class="sxs-lookup"><span data-stu-id="ccd30-122">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccd30-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="ccd30-123">-Name</span></span>
<span data-ttu-id="ccd30-124">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="ccd30-124">Key name.</span></span>
<span data-ttu-id="ccd30-125">Cmdlet konstruerar FQDN för en Key från valv namnet, den valda miljön och det här namnet.</span><span class="sxs-lookup"><span data-stu-id="ccd30-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccd30-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ccd30-126">-VaultName</span></span>
<span data-ttu-id="ccd30-127">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="ccd30-127">Vault name.</span></span>
<span data-ttu-id="ccd30-128">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="ccd30-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ccd30-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ccd30-129">-Confirm</span></span>
<span data-ttu-id="ccd30-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ccd30-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccd30-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccd30-131">-WhatIf</span></span>
<span data-ttu-id="ccd30-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ccd30-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccd30-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ccd30-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccd30-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd30-134">CommonParameters</span></span>
<span data-ttu-id="ccd30-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccd30-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd30-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccd30-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd30-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ccd30-137">INPUTS</span></span>

### <span data-ttu-id="ccd30-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ccd30-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="ccd30-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ccd30-139">OUTPUTS</span></span>

### <span data-ttu-id="ccd30-140">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ccd30-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="ccd30-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ccd30-141">NOTES</span></span>

## <span data-ttu-id="ccd30-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ccd30-142">RELATED LINKS</span></span>

[<span data-ttu-id="ccd30-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ccd30-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="ccd30-144">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ccd30-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="ccd30-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ccd30-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

