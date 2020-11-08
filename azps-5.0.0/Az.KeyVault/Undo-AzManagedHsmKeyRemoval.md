---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263006"
---
# <span data-ttu-id="8aa61-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="8aa61-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="8aa61-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8aa61-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa61-103">Återställer en borttagen rad i en hanterad HSM till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="8aa61-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="8aa61-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8aa61-104">SYNTAX</span></span>

### <span data-ttu-id="8aa61-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="8aa61-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8aa61-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8aa61-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aa61-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8aa61-107">DESCRIPTION</span></span>
<span data-ttu-id="8aa61-108">Med cmdleten **Undo-AzManagedHsmKeyRemoval** återställs en tidigare borttagen.</span><span class="sxs-lookup"><span data-stu-id="8aa61-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="8aa61-109">Den återställda knappen aktive ras och kan användas för alla vanliga viktiga operationer.</span><span class="sxs-lookup"><span data-stu-id="8aa61-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="8aa61-110">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="8aa61-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="8aa61-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8aa61-111">EXAMPLES</span></span>

### <span data-ttu-id="8aa61-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8aa61-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="8aa61-113">Det här kommandot återställer den testkey001 som du har tagit bort, i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="8aa61-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="8aa61-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8aa61-114">PARAMETERS</span></span>

### <span data-ttu-id="8aa61-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa61-115">-DefaultProfile</span></span>
<span data-ttu-id="8aa61-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8aa61-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8aa61-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="8aa61-117">-HsmName</span></span>
<span data-ttu-id="8aa61-118">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="8aa61-118">HSM name.</span></span> <span data-ttu-id="8aa61-119">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="8aa61-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="8aa61-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8aa61-120">-InputObject</span></span>
<span data-ttu-id="8aa61-121">Borttaget nyckeltal</span><span class="sxs-lookup"><span data-stu-id="8aa61-121">Deleted key object</span></span>

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

### <span data-ttu-id="8aa61-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8aa61-122">-Name</span></span>
<span data-ttu-id="8aa61-123">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="8aa61-123">Key name.</span></span>
<span data-ttu-id="8aa61-124">Cmdlet konstruerar FQDN för en Key från Managed HSM-namn, markerat miljö-och namn för tillfället.</span><span class="sxs-lookup"><span data-stu-id="8aa61-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="8aa61-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8aa61-125">-Confirm</span></span>
<span data-ttu-id="8aa61-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8aa61-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aa61-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aa61-127">-WhatIf</span></span>
<span data-ttu-id="8aa61-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8aa61-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aa61-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8aa61-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aa61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa61-130">CommonParameters</span></span>
<span data-ttu-id="8aa61-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aa61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa61-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aa61-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa61-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8aa61-133">INPUTS</span></span>

### <span data-ttu-id="8aa61-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8aa61-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="8aa61-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8aa61-135">OUTPUTS</span></span>

### <span data-ttu-id="8aa61-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8aa61-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="8aa61-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8aa61-137">NOTES</span></span>

## <span data-ttu-id="8aa61-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8aa61-138">RELATED LINKS</span></span>

[<span data-ttu-id="8aa61-139">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="8aa61-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="8aa61-140">Säkerhets kopiering-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="8aa61-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="8aa61-141">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="8aa61-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="8aa61-142">Återställ-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="8aa61-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="8aa61-143">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="8aa61-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="8aa61-144">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="8aa61-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)