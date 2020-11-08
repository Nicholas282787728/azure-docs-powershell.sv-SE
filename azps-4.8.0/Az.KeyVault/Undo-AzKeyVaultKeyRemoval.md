---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: c2b4fec2524ed3ddac62cf687af33ba3f76f13e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103202"
---
# <span data-ttu-id="8cbaa-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="8cbaa-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="8cbaa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8cbaa-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbaa-103">Återställer en borttagen Key i ett nyckelord till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="8cbaa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8cbaa-104">SYNTAX</span></span>

### <span data-ttu-id="8cbaa-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="8cbaa-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cbaa-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8cbaa-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cbaa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8cbaa-107">DESCRIPTION</span></span>
<span data-ttu-id="8cbaa-108">Med cmdleten **Undo-AzKeyVaultKeyRemoval** återställs en tidigare borttagen.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="8cbaa-109">Den återställda knappen aktive ras och kan användas för alla vanliga viktiga operationer.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="8cbaa-110">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="8cbaa-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8cbaa-111">EXAMPLES</span></span>

### <span data-ttu-id="8cbaa-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8cbaa-112">Example 1</span></span>
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

<span data-ttu-id="8cbaa-113">Det här kommandot återställer den MyKey som du har tagit bort, i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="8cbaa-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8cbaa-114">PARAMETERS</span></span>

### <span data-ttu-id="8cbaa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbaa-115">-DefaultProfile</span></span>
<span data-ttu-id="8cbaa-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="8cbaa-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cbaa-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cbaa-117">-InputObject</span></span>
<span data-ttu-id="8cbaa-118">Borttaget nyckeltal</span><span class="sxs-lookup"><span data-stu-id="8cbaa-118">Deleted key object</span></span>

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

### <span data-ttu-id="8cbaa-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="8cbaa-119">-Name</span></span>
<span data-ttu-id="8cbaa-120">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-120">Key name.</span></span>
<span data-ttu-id="8cbaa-121">Cmdlet konstruerar FQDN för en Key från valv namnet, den valda miljön och det här namnet.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cbaa-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8cbaa-122">-VaultName</span></span>
<span data-ttu-id="8cbaa-123">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-123">Vault name.</span></span>
<span data-ttu-id="8cbaa-124">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8cbaa-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8cbaa-125">-Confirm</span></span>
<span data-ttu-id="8cbaa-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cbaa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cbaa-127">-WhatIf</span></span>
<span data-ttu-id="8cbaa-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cbaa-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cbaa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbaa-130">CommonParameters</span></span>
<span data-ttu-id="8cbaa-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cbaa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbaa-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cbaa-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbaa-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8cbaa-133">INPUTS</span></span>

### <span data-ttu-id="8cbaa-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8cbaa-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="8cbaa-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8cbaa-135">OUTPUTS</span></span>

### <span data-ttu-id="8cbaa-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8cbaa-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="8cbaa-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8cbaa-137">NOTES</span></span>

## <span data-ttu-id="8cbaa-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8cbaa-138">RELATED LINKS</span></span>

[<span data-ttu-id="8cbaa-139">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8cbaa-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="8cbaa-140">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8cbaa-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="8cbaa-141">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8cbaa-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

