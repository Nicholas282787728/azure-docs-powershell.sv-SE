---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
ms.openlocfilehash: 831bcdb76a0f24a2935f2ffd2ed0bf7df1c10042
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929870"
---
# <span data-ttu-id="f4d11-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="f4d11-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="f4d11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4d11-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d11-103">Återställer en borttagen Key i ett nyckelord till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="f4d11-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4d11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4d11-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d11-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4d11-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d11-106">Med cmdleten **Undo-AzureKeyVaultKeyRemoval** återställs en tidigare borttagen.</span><span class="sxs-lookup"><span data-stu-id="f4d11-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="f4d11-107">Den återställda knappen aktive ras och kan användas för alla vanliga viktiga operationer.</span><span class="sxs-lookup"><span data-stu-id="f4d11-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="f4d11-108">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="f4d11-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="f4d11-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4d11-109">EXAMPLES</span></span>

### <span data-ttu-id="f4d11-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f4d11-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="f4d11-111">Det här kommandot återställer den MyKey som du har tagit bort, i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="f4d11-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="f4d11-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4d11-112">PARAMETERS</span></span>

### <span data-ttu-id="f4d11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d11-113">-DefaultProfile</span></span>
<span data-ttu-id="f4d11-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f4d11-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4d11-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4d11-115">-Name</span></span>
<span data-ttu-id="f4d11-116">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="f4d11-116">Key name.</span></span>
<span data-ttu-id="f4d11-117">Cmdlet konstruerar FQDN för en Key från valv namnet, den valda miljön och det här namnet.</span><span class="sxs-lookup"><span data-stu-id="f4d11-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4d11-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f4d11-118">-VaultName</span></span>
<span data-ttu-id="f4d11-119">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="f4d11-119">Vault name.</span></span>
<span data-ttu-id="f4d11-120">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="f4d11-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f4d11-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4d11-121">-Confirm</span></span>
<span data-ttu-id="f4d11-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4d11-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d11-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d11-123">-WhatIf</span></span>
<span data-ttu-id="f4d11-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4d11-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d11-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4d11-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d11-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d11-126">CommonParameters</span></span>
<span data-ttu-id="f4d11-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d11-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d11-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d11-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d11-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4d11-129">INPUTS</span></span>

### <span data-ttu-id="f4d11-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d11-130">System.String</span></span>

## <span data-ttu-id="f4d11-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4d11-131">OUTPUTS</span></span>

### <span data-ttu-id="f4d11-132">Microsoft. Azure. commands...</span><span class="sxs-lookup"><span data-stu-id="f4d11-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="f4d11-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4d11-133">NOTES</span></span>

## <span data-ttu-id="f4d11-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4d11-134">RELATED LINKS</span></span>

[<span data-ttu-id="f4d11-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f4d11-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="f4d11-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f4d11-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="f4d11-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f4d11-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

