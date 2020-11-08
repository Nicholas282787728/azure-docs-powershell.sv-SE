---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: fcedf52f75b73cc35b7f0e4fd0856600bca6fc71
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272715"
---
# <span data-ttu-id="03ebd-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="03ebd-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="03ebd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="03ebd-102">SYNOPSIS</span></span>

<span data-ttu-id="03ebd-103">Hämtar en lista över återställnings tjänstens valv.</span><span class="sxs-lookup"><span data-stu-id="03ebd-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="03ebd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="03ebd-104">SYNTAX</span></span>

### <span data-ttu-id="03ebd-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ebd-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03ebd-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03ebd-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03ebd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="03ebd-107">DESCRIPTION</span></span>

<span data-ttu-id="03ebd-108">Cmdleten **Get-AzRecoveryServicesVault** hämtar en lista över återställnings tjänst valv i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="03ebd-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="03ebd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="03ebd-109">EXAMPLES</span></span>

### <span data-ttu-id="03ebd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="03ebd-110">Example 1</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="03ebd-111">Hämta listan med valv i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="03ebd-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="03ebd-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="03ebd-112">Example 2</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="03ebd-113">Hämta listan med valv i resurs gruppen i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="03ebd-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="03ebd-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="03ebd-114">Example 3</span></span>

```powershell
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="03ebd-115">Hämta valvet i resurs gruppen med angivet namn.</span><span class="sxs-lookup"><span data-stu-id="03ebd-115">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="03ebd-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="03ebd-116">PARAMETERS</span></span>

### <span data-ttu-id="03ebd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ebd-117">-DefaultProfile</span></span>

<span data-ttu-id="03ebd-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="03ebd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03ebd-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="03ebd-119">-Name</span></span>

<span data-ttu-id="03ebd-120">Anger namnet på valvet du vill fråga efter.</span><span class="sxs-lookup"><span data-stu-id="03ebd-120">Specifies the name of the vault to query for.</span></span>

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

### <span data-ttu-id="03ebd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03ebd-121">-ResourceGroupName</span></span>

<span data-ttu-id="03ebd-122">Anger namnet på den Azure Resource-grupp från vilken det angivna Recovery Services-objektet ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="03ebd-122">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="03ebd-123">-Tagg</span><span class="sxs-lookup"><span data-stu-id="03ebd-123">-Tag</span></span>

<span data-ttu-id="03ebd-124">Anger taggarna som ska sökas efter</span><span class="sxs-lookup"><span data-stu-id="03ebd-124">Specifies the Tags to query for</span></span>

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

### <span data-ttu-id="03ebd-125">-TagName</span><span class="sxs-lookup"><span data-stu-id="03ebd-125">-TagName</span></span>

<span data-ttu-id="03ebd-126">Anger tangenten för tagg att fråga efter</span><span class="sxs-lookup"><span data-stu-id="03ebd-126">Specifies the Key of the Tag to query for</span></span>

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

### <span data-ttu-id="03ebd-127">-TagValue</span><span class="sxs-lookup"><span data-stu-id="03ebd-127">-TagValue</span></span>

<span data-ttu-id="03ebd-128">Anger värdet för taggen som du vill fråga efter</span><span class="sxs-lookup"><span data-stu-id="03ebd-128">Specifies the Value of the Tag to query for</span></span>

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

### <span data-ttu-id="03ebd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ebd-129">CommonParameters</span></span>
<span data-ttu-id="03ebd-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ebd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ebd-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03ebd-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ebd-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="03ebd-132">INPUTS</span></span>

### <span data-ttu-id="03ebd-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="03ebd-133">None</span></span>

## <span data-ttu-id="03ebd-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="03ebd-134">OUTPUTS</span></span>

### <span data-ttu-id="03ebd-135">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="03ebd-135">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="03ebd-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="03ebd-136">NOTES</span></span>
<span data-ttu-id="03ebd-137">Get-AzRecoveryServicesVault i den gamla versionen av AZ. RecoveryServices (<= 2.10.0) kan inte fungera med AZ. accounts (>= 1.8.1) på grund av fel sammansättnings referens.</span><span class="sxs-lookup"><span data-stu-id="03ebd-137">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="03ebd-138">Modulen AZ. RecoveryServices måste uppgraderas till 2.11.0 eller senare om du använder de senaste AZ eller AZ. accounts.</span><span class="sxs-lookup"><span data-stu-id="03ebd-138">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="03ebd-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="03ebd-139">RELATED LINKS</span></span>

[<span data-ttu-id="03ebd-140">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="03ebd-140">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="03ebd-141">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="03ebd-141">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="03ebd-142">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="03ebd-142">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
