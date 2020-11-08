---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: b7ee6a380bf7803913f3f302bee45bad62f106b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092442"
---
# <span data-ttu-id="7503d-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7503d-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="7503d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7503d-102">SYNOPSIS</span></span>

<span data-ttu-id="7503d-103">Hämtar en lista över återställnings tjänstens valv.</span><span class="sxs-lookup"><span data-stu-id="7503d-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="7503d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7503d-104">SYNTAX</span></span>

### <span data-ttu-id="7503d-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="7503d-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7503d-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7503d-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7503d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7503d-107">DESCRIPTION</span></span>

<span data-ttu-id="7503d-108">Cmdleten **Get-AzRecoveryServicesVault** hämtar en lista över återställnings tjänst valv i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="7503d-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="7503d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7503d-109">EXAMPLES</span></span>

### <span data-ttu-id="7503d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7503d-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="7503d-111">Hämta listan med valv i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7503d-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="7503d-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7503d-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="7503d-113">Hämta listan med valv i resurs gruppen i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="7503d-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="7503d-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7503d-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="7503d-115">Hämta valvet i resurs gruppen med angivet namn.</span><span class="sxs-lookup"><span data-stu-id="7503d-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="7503d-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7503d-116">PARAMETERS</span></span>

### <span data-ttu-id="7503d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7503d-117">-DefaultProfile</span></span>

<span data-ttu-id="7503d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7503d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7503d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="7503d-119">-Name</span></span>

<span data-ttu-id="7503d-120">Anger namnet på valvet du vill fråga efter.</span><span class="sxs-lookup"><span data-stu-id="7503d-120">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7503d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7503d-121">-ResourceGroupName</span></span>

<span data-ttu-id="7503d-122">Anger namnet på den Azure Resource-grupp från vilken det angivna Recovery Services-objektet ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="7503d-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7503d-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7503d-123">-Tag</span></span>

<span data-ttu-id="7503d-124">Anger taggarna som ska sökas efter</span><span class="sxs-lookup"><span data-stu-id="7503d-124">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7503d-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="7503d-125">-TagName</span></span>

<span data-ttu-id="7503d-126">Anger tangenten för tagg att fråga efter</span><span class="sxs-lookup"><span data-stu-id="7503d-126">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7503d-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="7503d-127">-TagValue</span></span>

<span data-ttu-id="7503d-128">Anger värdet för taggen som du vill fråga efter</span><span class="sxs-lookup"><span data-stu-id="7503d-128">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7503d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7503d-129">CommonParameters</span></span>
<span data-ttu-id="7503d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7503d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7503d-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7503d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7503d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7503d-132">INPUTS</span></span>

### <span data-ttu-id="7503d-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="7503d-133">None</span></span>

## <span data-ttu-id="7503d-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7503d-134">OUTPUTS</span></span>

### <span data-ttu-id="7503d-135">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="7503d-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7503d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7503d-136">NOTES</span></span>

## <span data-ttu-id="7503d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7503d-137">RELATED LINKS</span></span>

[<span data-ttu-id="7503d-138">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7503d-138">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="7503d-139">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7503d-139">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="7503d-140">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7503d-140">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
