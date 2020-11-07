---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
ms.openlocfilehash: a025dc40a666f643a3e7e232a22451e73f3e60bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929866"
---
# <span data-ttu-id="35d6b-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="35d6b-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="35d6b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="35d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="35d6b-103">Återställer en borttagen hemlighet i ett nyckel valv till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="35d6b-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35d6b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="35d6b-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35d6b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="35d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="35d6b-106">Cmdleten **Undo-AzureKeyVaultSecretRemoval** återställer en tidigare borttagen hemlighet.</span><span class="sxs-lookup"><span data-stu-id="35d6b-106">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="35d6b-107">Den återställda hemligheten aktive ras och kan användas för alla vanliga hemliga åtgärder.</span><span class="sxs-lookup"><span data-stu-id="35d6b-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="35d6b-108">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="35d6b-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="35d6b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="35d6b-109">EXAMPLES</span></span>

### <span data-ttu-id="35d6b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="35d6b-110">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="35d6b-111">Det här kommandot återställer hemligheten "hemlig" som tidigare har tagits bort i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="35d6b-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="35d6b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="35d6b-112">PARAMETERS</span></span>

### <span data-ttu-id="35d6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d6b-113">-DefaultProfile</span></span>
<span data-ttu-id="35d6b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="35d6b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35d6b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="35d6b-115">-Name</span></span>
<span data-ttu-id="35d6b-116">Hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="35d6b-116">Secret name.</span></span>
<span data-ttu-id="35d6b-117">Cmdlet konstruerar FQDN för en hemlighet från valv namn, för närvarande valt miljö och hemligt namn.</span><span class="sxs-lookup"><span data-stu-id="35d6b-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="35d6b-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="35d6b-118">-VaultName</span></span>
<span data-ttu-id="35d6b-119">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="35d6b-119">Vault name.</span></span>
<span data-ttu-id="35d6b-120">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="35d6b-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="35d6b-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="35d6b-121">-Confirm</span></span>
<span data-ttu-id="35d6b-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="35d6b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d6b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d6b-123">-WhatIf</span></span>
<span data-ttu-id="35d6b-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="35d6b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35d6b-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="35d6b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d6b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d6b-126">CommonParameters</span></span>
<span data-ttu-id="35d6b-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d6b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d6b-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35d6b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d6b-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="35d6b-129">INPUTS</span></span>

### <span data-ttu-id="35d6b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="35d6b-130">System.String</span></span>

## <span data-ttu-id="35d6b-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="35d6b-131">OUTPUTS</span></span>

### <span data-ttu-id="35d6b-132">Microsoft. Azure. commands. nyckel valv. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="35d6b-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="35d6b-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="35d6b-133">NOTES</span></span>

## <span data-ttu-id="35d6b-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="35d6b-134">RELATED LINKS</span></span>

[<span data-ttu-id="35d6b-135">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35d6b-135">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)



[<span data-ttu-id="35d6b-136">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="35d6b-136">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
