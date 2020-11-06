---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 70d6d39ed3e2083bf0f52e9e56808b7d36f1cc24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576502"
---
# <span data-ttu-id="e5d16-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e5d16-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e5d16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e5d16-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d16-103">Tar bort en certifikat åtgärd från ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="e5d16-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5d16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e5d16-104">SYNTAX</span></span>

### <span data-ttu-id="e5d16-105">Vis</span><span class="sxs-lookup"><span data-stu-id="e5d16-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5d16-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e5d16-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5d16-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e5d16-107">DESCRIPTION</span></span>
<span data-ttu-id="e5d16-108">Cmdleten **Remove-AzureKeyVaultCertificateOperation** tar bort en certifikat åtgärd från ett valv.</span><span class="sxs-lookup"><span data-stu-id="e5d16-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="e5d16-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e5d16-109">EXAMPLES</span></span>

### <span data-ttu-id="e5d16-110">Exempel 1: ta bort en certifikat åtgärd</span><span class="sxs-lookup"><span data-stu-id="e5d16-110">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="e5d16-111">Det här kommandot tar bort certifikat åtgärden som heter TestCert01 från ContosoKV01-valvet utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e5d16-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="e5d16-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e5d16-112">PARAMETERS</span></span>

### <span data-ttu-id="e5d16-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d16-113">-DefaultProfile</span></span>
<span data-ttu-id="e5d16-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="e5d16-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5d16-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e5d16-115">-Force</span></span>
<span data-ttu-id="e5d16-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e5d16-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d16-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5d16-117">-InputObject</span></span>
<span data-ttu-id="e5d16-118">Åtgärds objekt</span><span class="sxs-lookup"><span data-stu-id="e5d16-118">Operation object</span></span>

```yaml
Type: PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d16-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e5d16-119">-Name</span></span>
<span data-ttu-id="e5d16-120">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="e5d16-120">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d16-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5d16-121">-PassThru</span></span>
<span data-ttu-id="e5d16-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e5d16-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e5d16-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e5d16-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d16-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e5d16-124">-VaultName</span></span>
<span data-ttu-id="e5d16-125">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="e5d16-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="e5d16-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e5d16-126">-Confirm</span></span>
<span data-ttu-id="e5d16-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e5d16-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d16-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5d16-128">-WhatIf</span></span>
<span data-ttu-id="e5d16-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5d16-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5d16-130">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e5d16-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5d16-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e5d16-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5d16-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d16-132">CommonParameters</span></span>
<span data-ttu-id="e5d16-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d16-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d16-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5d16-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d16-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e5d16-135">INPUTS</span></span>

### <span data-ttu-id="e5d16-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="e5d16-136">None</span></span>
<span data-ttu-id="e5d16-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="e5d16-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5d16-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e5d16-138">OUTPUTS</span></span>

### <span data-ttu-id="e5d16-139">Microsoft. Azure. commands. valv. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e5d16-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="e5d16-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e5d16-140">NOTES</span></span>

## <span data-ttu-id="e5d16-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e5d16-141">RELATED LINKS</span></span>

[<span data-ttu-id="e5d16-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e5d16-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="e5d16-143">Stopp-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="e5d16-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

