---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 4c732cdfc175c47e9bd8125234cb1d33f1b19097
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928805"
---
# <span data-ttu-id="a0238-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a0238-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a0238-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0238-102">SYNOPSIS</span></span>
<span data-ttu-id="a0238-103">Tar bort en certifikat utfärdare från ett huvud valv.</span><span class="sxs-lookup"><span data-stu-id="a0238-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0238-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0238-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0238-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0238-105">DESCRIPTION</span></span>
<span data-ttu-id="a0238-106">Cmdleten **Remove-AzureKeyVaultCertificateIssuer** tar bort en certifikat utfärdare från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a0238-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="a0238-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0238-107">EXAMPLES</span></span>

### <span data-ttu-id="a0238-108">Exempel 1: ta bort en certifikat utfärdare</span><span class="sxs-lookup"><span data-stu-id="a0238-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="a0238-109">Det här kommandot tar bort certifikat utfärdaren som heter TestIssuer01 från ContosoKV01-.</span><span class="sxs-lookup"><span data-stu-id="a0238-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="a0238-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0238-110">PARAMETERS</span></span>

### <span data-ttu-id="a0238-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0238-111">-DefaultProfile</span></span>
<span data-ttu-id="a0238-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a0238-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0238-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a0238-113">-Force</span></span>
<span data-ttu-id="a0238-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a0238-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0238-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="a0238-115">-Name</span></span>
<span data-ttu-id="a0238-116">Anger namnet på den utfärdare som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a0238-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0238-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0238-117">-PassThru</span></span>
<span data-ttu-id="a0238-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="a0238-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a0238-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="a0238-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0238-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a0238-120">-VaultName</span></span>
<span data-ttu-id="a0238-121">Anger namnet på ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="a0238-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="a0238-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0238-122">-Confirm</span></span>
<span data-ttu-id="a0238-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0238-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0238-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0238-124">-WhatIf</span></span>
<span data-ttu-id="a0238-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0238-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0238-126">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0238-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0238-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0238-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0238-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0238-128">CommonParameters</span></span>
<span data-ttu-id="a0238-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0238-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0238-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0238-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0238-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0238-131">INPUTS</span></span>

## <span data-ttu-id="a0238-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0238-132">OUTPUTS</span></span>

### <span data-ttu-id="a0238-133">Microsoft. Azure. commands. valv. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a0238-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="a0238-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0238-134">NOTES</span></span>

## <span data-ttu-id="a0238-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0238-135">RELATED LINKS</span></span>

[<span data-ttu-id="a0238-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a0238-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="a0238-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="a0238-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


