---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 37cc2025b97e16a2af313a2f4dd2cf7dfe815b7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922689"
---
# <span data-ttu-id="a3064-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a3064-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a3064-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a3064-102">SYNOPSIS</span></span>
<span data-ttu-id="a3064-103">Tar bort en certifikat åtgärd från ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="a3064-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="a3064-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a3064-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3064-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a3064-105">DESCRIPTION</span></span>
<span data-ttu-id="a3064-106">Cmdleten **Remove-AzKeyVaultCertificateOperation** tar bort en certifikat åtgärd från ett valv.</span><span class="sxs-lookup"><span data-stu-id="a3064-106">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="a3064-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a3064-107">EXAMPLES</span></span>

### <span data-ttu-id="a3064-108">Exempel 1: ta bort en certifikat åtgärd</span><span class="sxs-lookup"><span data-stu-id="a3064-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="a3064-109">Det här kommandot tar bort certifikat åtgärden som heter TestCert01 från ContosoKV01-valvet utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a3064-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="a3064-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a3064-110">PARAMETERS</span></span>

### <span data-ttu-id="a3064-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3064-111">-DefaultProfile</span></span>
<span data-ttu-id="a3064-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a3064-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3064-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a3064-113">-Force</span></span>
<span data-ttu-id="a3064-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a3064-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a3064-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a3064-115">-Name</span></span>
<span data-ttu-id="a3064-116">Anger namnet på ett certifikat.</span><span class="sxs-lookup"><span data-stu-id="a3064-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3064-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3064-117">-PassThru</span></span>
<span data-ttu-id="a3064-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a3064-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a3064-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a3064-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a3064-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a3064-120">-VaultName</span></span>
<span data-ttu-id="a3064-121">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a3064-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a3064-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a3064-122">-Confirm</span></span>
<span data-ttu-id="a3064-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a3064-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3064-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3064-124">-WhatIf</span></span>
<span data-ttu-id="a3064-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3064-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3064-126">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a3064-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3064-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a3064-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3064-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3064-128">CommonParameters</span></span>
<span data-ttu-id="a3064-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3064-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3064-130">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3064-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3064-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a3064-131">INPUTS</span></span>

### <span data-ttu-id="a3064-132">Ingen</span><span class="sxs-lookup"><span data-stu-id="a3064-132">None</span></span>
<span data-ttu-id="a3064-133">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a3064-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3064-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a3064-134">OUTPUTS</span></span>

### <span data-ttu-id="a3064-135">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a3064-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="a3064-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a3064-136">NOTES</span></span>

## <span data-ttu-id="a3064-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a3064-137">RELATED LINKS</span></span>

[<span data-ttu-id="a3064-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a3064-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="a3064-139">Stopp-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="a3064-139">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

