---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 1fbf5a5541fe3e1360e696f9c06a26d6ea131dc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583300"
---
# <span data-ttu-id="39bf8-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="39bf8-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="39bf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="39bf8-103">Tar bort en kontakt som är registrerad för certifikat aviseringar från ett valv.</span><span class="sxs-lookup"><span data-stu-id="39bf8-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39bf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39bf8-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39bf8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="39bf8-106">Cmdleten **Remove-AzureKeyVaultCertificateContact** tar bort en kontakt som är registrerad för certifikat aviseringar från ett valv.</span><span class="sxs-lookup"><span data-stu-id="39bf8-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="39bf8-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="39bf8-108">Exempel 1: ta bort en certifikat kontakt</span><span class="sxs-lookup"><span data-stu-id="39bf8-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="39bf8-109">Det här kommandot tar bort Patti Nilsson som en certifikat kontakt för Contoso01-.</span><span class="sxs-lookup"><span data-stu-id="39bf8-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="39bf8-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39bf8-110">PARAMETERS</span></span>

### <span data-ttu-id="39bf8-111">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="39bf8-111">-EmailAddress</span></span>
<span data-ttu-id="39bf8-112">Anger e-postadressen till den kontakt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="39bf8-112">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39bf8-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39bf8-113">-PassThru</span></span>
<span data-ttu-id="39bf8-114">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="39bf8-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="39bf8-115">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="39bf8-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39bf8-116">-VaultName</span><span class="sxs-lookup"><span data-stu-id="39bf8-116">-VaultName</span></span>
<span data-ttu-id="39bf8-117">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="39bf8-117">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39bf8-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39bf8-118">-Confirm</span></span>
<span data-ttu-id="39bf8-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39bf8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39bf8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39bf8-120">-WhatIf</span></span>
<span data-ttu-id="39bf8-121">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39bf8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39bf8-122">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39bf8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39bf8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bf8-123">-DefaultProfile</span></span>
<span data-ttu-id="39bf8-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39bf8-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39bf8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bf8-125">CommonParameters</span></span>
<span data-ttu-id="39bf8-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39bf8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bf8-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39bf8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bf8-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39bf8-128">INPUTS</span></span>

## <span data-ttu-id="39bf8-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39bf8-129">OUTPUTS</span></span>

### <span data-ttu-id="39bf8-130">System. Collections. Generic. list ' 1 [Microsoft. Azure. commands. valv. Models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="39bf8-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="39bf8-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39bf8-131">NOTES</span></span>

## <span data-ttu-id="39bf8-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39bf8-132">RELATED LINKS</span></span>

[<span data-ttu-id="39bf8-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="39bf8-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="39bf8-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="39bf8-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

