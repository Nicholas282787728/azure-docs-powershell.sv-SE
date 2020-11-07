---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 5b0e67fbbead536803dba8efeb2c8a61d7f75c5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924425"
---
# <span data-ttu-id="17102-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="17102-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="17102-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17102-102">SYNOPSIS</span></span>
<span data-ttu-id="17102-103">Återställer en borttagen Key i ett nyckelord till ett aktivt tillstånd.</span><span class="sxs-lookup"><span data-stu-id="17102-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="17102-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17102-104">SYNTAX</span></span>

```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17102-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17102-105">DESCRIPTION</span></span>
<span data-ttu-id="17102-106">Med cmdleten **Undo-AzKeyVaultKeyRemoval** återställs en tidigare borttagen.</span><span class="sxs-lookup"><span data-stu-id="17102-106">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="17102-107">Den återställda knappen aktive ras och kan användas för alla vanliga viktiga operationer.</span><span class="sxs-lookup"><span data-stu-id="17102-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="17102-108">Den som ringer måste ha behörigheten "återfå" för att kunna utföra den här åtgärden.</span><span class="sxs-lookup"><span data-stu-id="17102-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="17102-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17102-109">EXAMPLES</span></span>

### <span data-ttu-id="17102-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17102-110">Example 1</span></span>
```
PS C:\>Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="17102-111">Det här kommandot återställer den MyKey som du har tagit bort, i ett aktivt och användbart tillstånd.</span><span class="sxs-lookup"><span data-stu-id="17102-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="17102-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17102-112">PARAMETERS</span></span>

### <span data-ttu-id="17102-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17102-113">-DefaultProfile</span></span>
<span data-ttu-id="17102-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="17102-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17102-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="17102-115">-Name</span></span>
<span data-ttu-id="17102-116">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="17102-116">Key name.</span></span>
<span data-ttu-id="17102-117">Cmdlet konstruerar FQDN för en Key från valv namnet, den valda miljön och det här namnet.</span><span class="sxs-lookup"><span data-stu-id="17102-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="17102-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="17102-118">-VaultName</span></span>
<span data-ttu-id="17102-119">Valv namn.</span><span class="sxs-lookup"><span data-stu-id="17102-119">Vault name.</span></span>
<span data-ttu-id="17102-120">Cmdlet konstruerar FQDN för ett valv baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="17102-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="17102-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17102-121">-Confirm</span></span>
<span data-ttu-id="17102-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17102-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17102-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17102-123">-WhatIf</span></span>
<span data-ttu-id="17102-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17102-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17102-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17102-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17102-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17102-126">CommonParameters</span></span>
<span data-ttu-id="17102-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17102-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17102-128">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17102-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17102-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17102-129">INPUTS</span></span>

### <span data-ttu-id="17102-130">System. String</span><span class="sxs-lookup"><span data-stu-id="17102-130">System.String</span></span>

## <span data-ttu-id="17102-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17102-131">OUTPUTS</span></span>

### <span data-ttu-id="17102-132">Microsoft. Azure. commands...</span><span class="sxs-lookup"><span data-stu-id="17102-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="17102-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17102-133">NOTES</span></span>

## <span data-ttu-id="17102-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17102-134">RELATED LINKS</span></span>

[<span data-ttu-id="17102-135">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="17102-135">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="17102-136">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="17102-136">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="17102-137">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="17102-137">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

