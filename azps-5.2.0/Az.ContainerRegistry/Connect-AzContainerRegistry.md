---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/connect-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Connect-AzContainerRegistry.md
ms.openlocfilehash: 806fb4892e0fa68b8e49fe29ec0897abf9be2dc8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400907"
---
# <span data-ttu-id="165f2-101">Connect-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="165f2-101">Connect-AzContainerRegistry</span></span>

## <span data-ttu-id="165f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="165f2-102">SYNOPSIS</span></span>
<span data-ttu-id="165f2-103">Logga in på en Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="165f2-103">Login to an azure container registry.</span></span>

## <span data-ttu-id="165f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="165f2-104">SYNTAX</span></span>

### <span data-ttu-id="165f2-105">WithoutNameAndPasswordParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="165f2-105">WithoutNameAndPasswordParameterSet (Default)</span></span>
```
Connect-AzContainerRegistry -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="165f2-106">WithNameAndPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="165f2-106">WithNameAndPasswordParameterSet</span></span>
```
Connect-AzContainerRegistry -Name <String> -UserName <String> -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="165f2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="165f2-107">DESCRIPTION</span></span>
<span data-ttu-id="165f2-108">Logga in på en Azure-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="165f2-108">Login to an azure container registry.</span></span>

## <span data-ttu-id="165f2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="165f2-109">EXAMPLES</span></span>

### <span data-ttu-id="165f2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="165f2-110">Example 1</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName
```

<span data-ttu-id="165f2-111">Logga in på ACR utan autentiseringsuppgifter när du redan har loggat in på Azure-kontot.</span><span class="sxs-lookup"><span data-stu-id="165f2-111">Login to ACR with no credentials when already login to azure account.</span></span>

### <span data-ttu-id="165f2-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="165f2-112">Example 2</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $RegistryName -Password $AdminPassWord
```

<span data-ttu-id="165f2-113">Logga in på ACR med administratörs användar namn/lösen ord när administratörs användaren aktiverade.</span><span class="sxs-lookup"><span data-stu-id="165f2-113">Login to ACR with admin username/password when admin user was enabled.</span></span>

### <span data-ttu-id="165f2-114">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="165f2-114">Example 3</span></span>
```powershell
PS C:\> Connect-AzContainerRegistry -Name $RegistryName -UserName $ServicePrincipal -Password $ServicePrincipalPassword
```

<span data-ttu-id="165f2-115">Logga in på ACR med ID och lösen ord för tjänstens huvud program.</span><span class="sxs-lookup"><span data-stu-id="165f2-115">Login to ACR with service principal application ID and password.</span></span>

## <span data-ttu-id="165f2-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="165f2-116">PARAMETERS</span></span>

### <span data-ttu-id="165f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="165f2-117">-DefaultProfile</span></span>
<span data-ttu-id="165f2-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="165f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="165f2-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="165f2-119">-Name</span></span>
<span data-ttu-id="165f2-120">Namn på Azure-behållare.</span><span class="sxs-lookup"><span data-stu-id="165f2-120">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="165f2-121">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="165f2-121">-Password</span></span>
<span data-ttu-id="165f2-122">Lösen ord för Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="165f2-122">Password For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="165f2-123">-UserName</span><span class="sxs-lookup"><span data-stu-id="165f2-123">-UserName</span></span>
<span data-ttu-id="165f2-124">Användar namn för Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="165f2-124">User Name For Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: WithNameAndPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="165f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="165f2-125">CommonParameters</span></span>
<span data-ttu-id="165f2-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="165f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="165f2-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="165f2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="165f2-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="165f2-128">INPUTS</span></span>

### <span data-ttu-id="165f2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="165f2-129">System.String</span></span>

## <span data-ttu-id="165f2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="165f2-130">OUTPUTS</span></span>

### <span data-ttu-id="165f2-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="165f2-131">System.Boolean</span></span>

## <span data-ttu-id="165f2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="165f2-132">NOTES</span></span>

## <span data-ttu-id="165f2-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="165f2-133">RELATED LINKS</span></span>
