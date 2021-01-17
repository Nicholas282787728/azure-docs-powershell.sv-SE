---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 94f27b497450201715b423babbd55811f2382dd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418083"
---
# <span data-ttu-id="89568-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="89568-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="89568-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="89568-102">SYNOPSIS</span></span>
<span data-ttu-id="89568-103">Exporterar säkerhets domän data för en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="89568-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="89568-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="89568-104">SYNTAX</span></span>

### <span data-ttu-id="89568-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="89568-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89568-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="89568-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89568-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="89568-107">DESCRIPTION</span></span>
<span data-ttu-id="89568-108">Exporterar säkerhets domän data för en hanterad HSM för import på en annan HSM.</span><span class="sxs-lookup"><span data-stu-id="89568-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="89568-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="89568-109">EXAMPLES</span></span>

### <span data-ttu-id="89568-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="89568-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="89568-111">Det här kommandot hämtar den hanterade HSM som heter testmhsm och sparar en säkerhets kopia av den hanterade HSM-säkerhets domänen i den angivna utdatafilen.</span><span class="sxs-lookup"><span data-stu-id="89568-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="89568-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="89568-112">PARAMETERS</span></span>

### <span data-ttu-id="89568-113">-Certifikat</span><span class="sxs-lookup"><span data-stu-id="89568-113">-Certificates</span></span>
<span data-ttu-id="89568-114">Sökvägar till de certifikat som används för att kryptera säkerhets domän data.</span><span class="sxs-lookup"><span data-stu-id="89568-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89568-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89568-115">-DefaultProfile</span></span>
<span data-ttu-id="89568-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="89568-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89568-117">-Force</span><span class="sxs-lookup"><span data-stu-id="89568-117">-Force</span></span>
<span data-ttu-id="89568-118">Ange om du vill skriva över den befintliga filen.</span><span class="sxs-lookup"><span data-stu-id="89568-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="89568-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89568-119">-InputObject</span></span>
<span data-ttu-id="89568-120">Objekt som representerar en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="89568-120">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89568-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="89568-121">-Name</span></span>
<span data-ttu-id="89568-122">Namnet på den hanterade HSM.</span><span class="sxs-lookup"><span data-stu-id="89568-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89568-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="89568-123">-OutputPath</span></span>
<span data-ttu-id="89568-124">Ange sökvägen till säkerhets domän data som ska hämtas till.</span><span class="sxs-lookup"><span data-stu-id="89568-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89568-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89568-125">-PassThru</span></span>
<span data-ttu-id="89568-126">När det anges returneras ett booleskt värde när cmdleten lyckas.</span><span class="sxs-lookup"><span data-stu-id="89568-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="89568-127">-Kvorum</span><span class="sxs-lookup"><span data-stu-id="89568-127">-Quorum</span></span>
<span data-ttu-id="89568-128">Det minsta antalet resurser som behövs för att dekryptera säkerhets domänen för återställning.</span><span class="sxs-lookup"><span data-stu-id="89568-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89568-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="89568-129">-Confirm</span></span>
<span data-ttu-id="89568-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="89568-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89568-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89568-131">-WhatIf</span></span>
<span data-ttu-id="89568-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="89568-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89568-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="89568-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89568-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89568-134">CommonParameters</span></span>
<span data-ttu-id="89568-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89568-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89568-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89568-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89568-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="89568-137">INPUTS</span></span>

### <span data-ttu-id="89568-138">Microsoft. Azure. commands. valv. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="89568-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="89568-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="89568-139">OUTPUTS</span></span>

### <span data-ttu-id="89568-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89568-140">System.Boolean</span></span>

## <span data-ttu-id="89568-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="89568-141">NOTES</span></span>

## <span data-ttu-id="89568-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="89568-142">RELATED LINKS</span></span>
