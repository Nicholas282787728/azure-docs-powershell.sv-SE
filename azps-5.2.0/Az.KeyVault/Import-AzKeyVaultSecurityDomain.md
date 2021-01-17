---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/import-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Import-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: f96aa323486144ec9d4dcb04ff00f408a763a81a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411736"
---
# <span data-ttu-id="92d3d-101">Import-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="92d3d-101">Import-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="92d3d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="92d3d-103">Importerar tidigare exporterade säkerhets domän data till en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="92d3d-103">Imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="92d3d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92d3d-104">SYNTAX</span></span>

### <span data-ttu-id="92d3d-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="92d3d-105">ByName (Default)</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92d3d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92d3d-106">ByInputObject</span></span>
```
Import-AzKeyVaultSecurityDomain -Keys <KeyPath[]> -SecurityDomainPath <String> [-PassThru]
 -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92d3d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92d3d-107">DESCRIPTION</span></span>
<span data-ttu-id="92d3d-108">Denna cmdlet importerar tidigare exporterade säkerhets domän data till en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="92d3d-108">This cmdlet imports previously exported security domain data to a managed HSM.</span></span>

## <span data-ttu-id="92d3d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92d3d-109">EXAMPLES</span></span>

### <span data-ttu-id="92d3d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="92d3d-110">Example 1</span></span>
```powershell
PS C:\> $keys = @{PublicKey = "sd1.cer"; PrivateKey = "sd1.key"}, @{PublicKey = "sd2.cer"; PrivateKey = "sd2.key"}, @{PublicKey = "sd3.cer"; PrivateKey = "sd3.key"}
PS C:\> Import-AzKeyVaultSecurityDomain -Name testmhsm -Keys $keys -SecurityDomainPath {pathOfBackup}\sd.ps.json
```

<span data-ttu-id="92d3d-111">Först måste nycklarna tillhandahållas för att dekryptera säkerhets domän data.</span><span class="sxs-lookup"><span data-stu-id="92d3d-111">First, the keys need be provided to decrypt the security domain data.</span></span>
<span data-ttu-id="92d3d-112">Då återställer kommandot **import-AzKeyVaultSecurityDomain** säkerhets domän data som har säkerhetskopierats till en hanterad HSM med de här nycklarna.</span><span class="sxs-lookup"><span data-stu-id="92d3d-112">Then, The **Import-AzKeyVaultSecurityDomain** command restores previous backed up security domain data to a managed HSM using these keys.</span></span>

## <span data-ttu-id="92d3d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92d3d-113">PARAMETERS</span></span>

### <span data-ttu-id="92d3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92d3d-114">-DefaultProfile</span></span>
<span data-ttu-id="92d3d-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="92d3d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92d3d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92d3d-116">-InputObject</span></span>
<span data-ttu-id="92d3d-117">Objekt som representerar en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="92d3d-117">Object representing a managed HSM.</span></span>

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

### <span data-ttu-id="92d3d-118">-Tangenter</span><span class="sxs-lookup"><span data-stu-id="92d3d-118">-Keys</span></span>
<span data-ttu-id="92d3d-119">Information om de nycklar som används för att dekryptera säkerhets domän data.</span><span class="sxs-lookup"><span data-stu-id="92d3d-119">Information about the keys that are used to decrypt the security domain data.</span></span>
<span data-ttu-id="92d3d-120">Se exempel på hur den är konstruerad.</span><span class="sxs-lookup"><span data-stu-id="92d3d-120">See examples for how it is constructed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.SecurityDomain.Models.KeyPath[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d3d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="92d3d-121">-Name</span></span>
<span data-ttu-id="92d3d-122">Namnet på den hanterade HSM.</span><span class="sxs-lookup"><span data-stu-id="92d3d-122">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="92d3d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92d3d-123">-PassThru</span></span>
<span data-ttu-id="92d3d-124">När det anges returneras ett booleskt värde när cmdleten lyckas.</span><span class="sxs-lookup"><span data-stu-id="92d3d-124">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="92d3d-125">-SecurityDomainPath</span><span class="sxs-lookup"><span data-stu-id="92d3d-125">-SecurityDomainPath</span></span>
<span data-ttu-id="92d3d-126">Ange sökvägen till den krypterade säkerhets domän informationen.</span><span class="sxs-lookup"><span data-stu-id="92d3d-126">Specify the path to the encrypted security domain data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92d3d-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="92d3d-127">-Confirm</span></span>
<span data-ttu-id="92d3d-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="92d3d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92d3d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92d3d-129">-WhatIf</span></span>
<span data-ttu-id="92d3d-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="92d3d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92d3d-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="92d3d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92d3d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92d3d-132">CommonParameters</span></span>
<span data-ttu-id="92d3d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92d3d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92d3d-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="92d3d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92d3d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92d3d-135">INPUTS</span></span>

### <span data-ttu-id="92d3d-136">Microsoft. Azure. commands. valv. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="92d3d-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="92d3d-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92d3d-137">OUTPUTS</span></span>

### <span data-ttu-id="92d3d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92d3d-138">System.Boolean</span></span>

## <span data-ttu-id="92d3d-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92d3d-139">NOTES</span></span>

## <span data-ttu-id="92d3d-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92d3d-140">RELATED LINKS</span></span>
