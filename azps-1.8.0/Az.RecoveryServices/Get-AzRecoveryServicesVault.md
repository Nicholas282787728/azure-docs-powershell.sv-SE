---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: 5dfe76ad08c59a661d6907c65a53da9397f0a66d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747407"
---
# <span data-ttu-id="9f7e3-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9f7e3-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="9f7e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f7e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f7e3-103">Hämtar en lista över återställnings tjänstens valv.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="9f7e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f7e3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVault [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f7e3-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f7e3-105">DESCRIPTION</span></span>
<span data-ttu-id="9f7e3-106">Cmdleten **Get-AzRecoveryServicesVault** hämtar en lista över återställnings tjänst valv i den aktuella prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-106">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="9f7e3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f7e3-107">EXAMPLES</span></span>

### <span data-ttu-id="9f7e3-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9f7e3-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="9f7e3-109">Hämta listan med valv i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-109">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="9f7e3-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9f7e3-110">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="9f7e3-111">Hämta listan med valv i resurs gruppen i det valda abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-111">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="9f7e3-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9f7e3-112">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
```

<span data-ttu-id="9f7e3-113">Hämta valvet i resurs gruppen med angivet namn.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-113">Get the vault in resource group with given name.</span></span>

## <span data-ttu-id="9f7e3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f7e3-114">PARAMETERS</span></span>

### <span data-ttu-id="9f7e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f7e3-115">-DefaultProfile</span></span>
<span data-ttu-id="9f7e3-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f7e3-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="9f7e3-117">-Name</span></span>
<span data-ttu-id="9f7e3-118">Anger namnet på valvet du vill fråga efter.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-118">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7e3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f7e3-119">-ResourceGroupName</span></span>
<span data-ttu-id="9f7e3-120">Anger namnet på den Azure-adressresurs som du vill skapa eller från vilken det angivna Recovery Services-objektet ska hämtas.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-120">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7e3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f7e3-121">CommonParameters</span></span>
<span data-ttu-id="9f7e3-122">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f7e3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f7e3-123">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f7e3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f7e3-124">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f7e3-124">INPUTS</span></span>

### <span data-ttu-id="9f7e3-125">Ingen</span><span class="sxs-lookup"><span data-stu-id="9f7e3-125">None</span></span>

## <span data-ttu-id="9f7e3-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f7e3-126">OUTPUTS</span></span>

### <span data-ttu-id="9f7e3-127">Microsoft. Azure. commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="9f7e3-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9f7e3-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f7e3-128">NOTES</span></span>

## <span data-ttu-id="9f7e3-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f7e3-129">RELATED LINKS</span></span>

[<span data-ttu-id="9f7e3-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="9f7e3-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="9f7e3-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9f7e3-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="9f7e3-132">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9f7e3-132">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


