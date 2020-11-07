---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: e71fa3098003f6fb713c90903eee6e97ca4f42ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756952"
---
# <span data-ttu-id="6fc42-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="6fc42-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="6fc42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6fc42-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc42-103">Återställer en borttagen hemlighet i ett nyckel valv till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="6fc42-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fc42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6fc42-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fc42-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6fc42-105">DESCRIPTION</span></span>
<span data-ttu-id="6fc42-106">Cmdleten **Undo-AzureKeyVaultSecretRemoval** återställer en tidigare borttagen hemlighet.</span><span class="sxs-lookup"><span data-stu-id="6fc42-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="6fc42-107">Den återställda hemligheten aktive ras och kan användas för alla vanliga hemliga åtgärder.</span><span class="sxs-lookup"><span data-stu-id="6fc42-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="6fc42-108">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="6fc42-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="6fc42-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6fc42-109">EXAMPLES</span></span>

### <span data-ttu-id="6fc42-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6fc42-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="6fc42-111">Det här kommandot återställer hemligheten "hemlig" som tidigare har tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="6fc42-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="6fc42-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6fc42-112">PARAMETERS</span></span>

### <span data-ttu-id="6fc42-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="6fc42-113">-Name</span></span>
<span data-ttu-id="6fc42-114">Hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="6fc42-114">Secret name.</span></span>
<span data-ttu-id="6fc42-115">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="6fc42-115">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc42-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6fc42-116">-VaultName</span></span>
<span data-ttu-id="6fc42-117">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="6fc42-117">Vault name.</span></span>
<span data-ttu-id="6fc42-118">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="6fc42-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc42-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6fc42-119">-Confirm</span></span>
<span data-ttu-id="6fc42-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6fc42-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fc42-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fc42-121">-WhatIf</span></span>
<span data-ttu-id="6fc42-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6fc42-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fc42-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6fc42-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fc42-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc42-124">-DefaultProfile</span></span>
<span data-ttu-id="6fc42-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6fc42-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fc42-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc42-126">CommonParameters</span></span>
<span data-ttu-id="6fc42-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc42-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc42-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc42-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc42-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6fc42-129">INPUTS</span></span>

### <span data-ttu-id="6fc42-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6fc42-130">System.String</span></span>

## <span data-ttu-id="6fc42-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6fc42-131">OUTPUTS</span></span>

### <span data-ttu-id="6fc42-132">Microsoft. Azure. commands. nyckel valv. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="6fc42-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="6fc42-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6fc42-133">NOTES</span></span>

## <span data-ttu-id="6fc42-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6fc42-134">RELATED LINKS</span></span>

[<span data-ttu-id="6fc42-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6fc42-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="6fc42-136">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6fc42-136">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="6fc42-137">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="6fc42-137">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
