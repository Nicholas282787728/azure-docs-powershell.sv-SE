---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: e65bef4119c51b989287bbf0db2e7587fef50271
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924414"
---
# <span data-ttu-id="71a8a-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="71a8a-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="71a8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="71a8a-103">Återställer en borttagen hemlighet i ett nyckel valv till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="71a8a-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="71a8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71a8a-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71a8a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="71a8a-106">Cmdleten **Undo-AzKeyVaultSecretRemoval** återställer en tidigare borttagen hemlighet.</span><span class="sxs-lookup"><span data-stu-id="71a8a-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="71a8a-107">Den återställda hemligheten aktive ras och kan användas för alla vanliga hemliga åtgärder.</span><span class="sxs-lookup"><span data-stu-id="71a8a-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="71a8a-108">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="71a8a-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="71a8a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71a8a-109">EXAMPLES</span></span>

### <span data-ttu-id="71a8a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="71a8a-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="71a8a-111">Det här kommandot återställer hemligheten "hemlig" som tidigare har tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="71a8a-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="71a8a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71a8a-112">PARAMETERS</span></span>

### <span data-ttu-id="71a8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a8a-113">-DefaultProfile</span></span>
<span data-ttu-id="71a8a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="71a8a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71a8a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="71a8a-115">-Name</span></span>
<span data-ttu-id="71a8a-116">Hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="71a8a-116">Secret name.</span></span>
<span data-ttu-id="71a8a-117">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="71a8a-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a8a-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="71a8a-118">-VaultName</span></span>
<span data-ttu-id="71a8a-119">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="71a8a-119">Vault name.</span></span>
<span data-ttu-id="71a8a-120">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="71a8a-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="71a8a-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71a8a-121">-Confirm</span></span>
<span data-ttu-id="71a8a-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71a8a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71a8a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a8a-123">-WhatIf</span></span>
<span data-ttu-id="71a8a-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71a8a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a8a-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71a8a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71a8a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a8a-126">CommonParameters</span></span>
<span data-ttu-id="71a8a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71a8a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a8a-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a8a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a8a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71a8a-129">INPUTS</span></span>

### <span data-ttu-id="71a8a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71a8a-130">System.String</span></span>

## <span data-ttu-id="71a8a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71a8a-131">OUTPUTS</span></span>

### <span data-ttu-id="71a8a-132">Microsoft. Azure. commands. nyckel valv. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="71a8a-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="71a8a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71a8a-133">NOTES</span></span>

## <span data-ttu-id="71a8a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71a8a-134">RELATED LINKS</span></span>

[<span data-ttu-id="71a8a-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="71a8a-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="71a8a-136">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="71a8a-136">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="71a8a-137">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="71a8a-137">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
