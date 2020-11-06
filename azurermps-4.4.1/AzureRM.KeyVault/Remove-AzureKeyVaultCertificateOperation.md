---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: d40489471e94474e83243803b5c64cdad1d572d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583296"
---
# <span data-ttu-id="7bb2f-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7bb2f-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7bb2f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7bb2f-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb2f-103">Tar bort en certifikat åtgärd från ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bb2f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7bb2f-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb2f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7bb2f-105">DESCRIPTION</span></span>
<span data-ttu-id="7bb2f-106">Cmdleten **Remove-AzureKeyVaultCertificateOperation** tar bort en certifikat åtgärd från ett valv.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="7bb2f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7bb2f-107">EXAMPLES</span></span>

### <span data-ttu-id="7bb2f-108">Exempel 1: ta bort en certifikat åtgärd</span><span class="sxs-lookup"><span data-stu-id="7bb2f-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="7bb2f-109">Det här kommandot tar bort certifikat åtgärden som heter TestCert01 från ContosoKV01-valvet utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="7bb2f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7bb2f-110">PARAMETERS</span></span>

### <span data-ttu-id="7bb2f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7bb2f-111">-Force</span></span>
<span data-ttu-id="7bb2f-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7bb2f-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="7bb2f-113">-Name</span></span>
<span data-ttu-id="7bb2f-114">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-114">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7bb2f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7bb2f-115">-PassThru</span></span>
<span data-ttu-id="7bb2f-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7bb2f-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7bb2f-118">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7bb2f-118">-VaultName</span></span>
<span data-ttu-id="7bb2f-119">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7bb2f-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7bb2f-120">-Confirm</span></span>
<span data-ttu-id="7bb2f-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb2f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb2f-122">-WhatIf</span></span>
<span data-ttu-id="7bb2f-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb2f-124">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bb2f-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bb2f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb2f-126">-DefaultProfile</span></span>
<span data-ttu-id="7bb2f-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bb2f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb2f-128">CommonParameters</span></span>
<span data-ttu-id="7bb2f-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb2f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb2f-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bb2f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb2f-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7bb2f-131">INPUTS</span></span>

## <span data-ttu-id="7bb2f-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7bb2f-132">OUTPUTS</span></span>

### <span data-ttu-id="7bb2f-133">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7bb2f-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="7bb2f-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7bb2f-134">NOTES</span></span>

## <span data-ttu-id="7bb2f-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7bb2f-135">RELATED LINKS</span></span>

[<span data-ttu-id="7bb2f-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7bb2f-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="7bb2f-137">Stopp-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="7bb2f-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

