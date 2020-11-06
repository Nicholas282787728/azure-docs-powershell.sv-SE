---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 29a7c2d3bb2060b77871cea0c088c50a59197cb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574284"
---
# <span data-ttu-id="179e3-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="179e3-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="179e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="179e3-102">SYNOPSIS</span></span>
<span data-ttu-id="179e3-103">Återställer en borttagen Key i ett nyckelord till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="179e3-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="179e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="179e3-104">SYNTAX</span></span>

### <span data-ttu-id="179e3-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="179e3-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="179e3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="179e3-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="179e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="179e3-107">DESCRIPTION</span></span>
<span data-ttu-id="179e3-108">Med cmdleten **Undo-AzureKeyVaultKeyRemoval** återställs en tidigare borttagen.</span><span class="sxs-lookup"><span data-stu-id="179e3-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="179e3-109">Den återställda knappen aktive ras och kan användas för alla vanliga viktiga operationer.</span><span class="sxs-lookup"><span data-stu-id="179e3-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="179e3-110">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="179e3-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="179e3-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="179e3-111">EXAMPLES</span></span>

### <span data-ttu-id="179e3-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="179e3-112">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="179e3-113">Det här kommandot återställer den MyKey som du har tagit bort, i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="179e3-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="179e3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="179e3-114">PARAMETERS</span></span>

### <span data-ttu-id="179e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="179e3-115">-DefaultProfile</span></span>
<span data-ttu-id="179e3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="179e3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="179e3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="179e3-117">-InputObject</span></span>
<span data-ttu-id="179e3-118">Borttaget nyckeltal</span><span class="sxs-lookup"><span data-stu-id="179e3-118">Deleted key object</span></span>

```yaml
Type: PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="179e3-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="179e3-119">-Name</span></span>
<span data-ttu-id="179e3-120">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="179e3-120">Key name.</span></span>
<span data-ttu-id="179e3-121">Cmdlet konstruerar FQDN för en Key från valv namnet, den valda miljön och det här namnet.</span><span class="sxs-lookup"><span data-stu-id="179e3-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="179e3-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="179e3-122">-VaultName</span></span>
<span data-ttu-id="179e3-123">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="179e3-123">Vault name.</span></span>
<span data-ttu-id="179e3-124">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="179e3-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="179e3-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="179e3-125">-Confirm</span></span>
<span data-ttu-id="179e3-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="179e3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="179e3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="179e3-127">-WhatIf</span></span>
<span data-ttu-id="179e3-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="179e3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="179e3-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="179e3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="179e3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="179e3-130">CommonParameters</span></span>
<span data-ttu-id="179e3-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="179e3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="179e3-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="179e3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="179e3-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="179e3-133">INPUTS</span></span>

### <span data-ttu-id="179e3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="179e3-134">System.String</span></span>

## <span data-ttu-id="179e3-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="179e3-135">OUTPUTS</span></span>

### <span data-ttu-id="179e3-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="179e3-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="179e3-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="179e3-137">NOTES</span></span>

## <span data-ttu-id="179e3-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="179e3-138">RELATED LINKS</span></span>

[<span data-ttu-id="179e3-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="179e3-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="179e3-140">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="179e3-140">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="179e3-141">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="179e3-141">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

