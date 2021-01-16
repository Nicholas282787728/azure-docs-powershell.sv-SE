---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: a53f67c12a5c8d125319fc19f69db3ea9a57c5e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407832"
---
# <span data-ttu-id="e55a6-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="e55a6-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="e55a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e55a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e55a6-103">Skapar en ny användare för enheten.</span><span class="sxs-lookup"><span data-stu-id="e55a6-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="e55a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e55a6-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e55a6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e55a6-105">DESCRIPTION</span></span>
<span data-ttu-id="e55a6-106">Den **nya AzDataBoxEdgeUser-** cmdleten skapar en ny användare för data Box Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="e55a6-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="e55a6-107">Det går bara att skapa en typ av användare `Share` .</span><span class="sxs-lookup"><span data-stu-id="e55a6-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="e55a6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e55a6-108">EXAMPLES</span></span>

### <span data-ttu-id="e55a6-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e55a6-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="e55a6-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e55a6-110">PARAMETERS</span></span>

### <span data-ttu-id="e55a6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e55a6-111">-AsJob</span></span>
<span data-ttu-id="e55a6-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e55a6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e55a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e55a6-113">-DefaultProfile</span></span>
<span data-ttu-id="e55a6-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e55a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e55a6-115">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="e55a6-115">-DeviceName</span></span>
<span data-ttu-id="e55a6-116">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="e55a6-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55a6-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e55a6-117">-EncryptionKey</span></span>
<span data-ttu-id="e55a6-118">Enhetens krypterings nycklar</span><span class="sxs-lookup"><span data-stu-id="e55a6-118">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55a6-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e55a6-119">-Name</span></span>
<span data-ttu-id="e55a6-120">Namnen</span><span class="sxs-lookup"><span data-stu-id="e55a6-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55a6-121">-Lösen ord</span><span class="sxs-lookup"><span data-stu-id="e55a6-121">-Password</span></span>
<span data-ttu-id="e55a6-122">Lösen ord, ange som en säker sträng</span><span class="sxs-lookup"><span data-stu-id="e55a6-122">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e55a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="e55a6-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e55a6-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55a6-125">– Skriv</span><span class="sxs-lookup"><span data-stu-id="e55a6-125">-Type</span></span>
<span data-ttu-id="e55a6-126">Välj UserType</span><span class="sxs-lookup"><span data-stu-id="e55a6-126">Select UserType</span></span>

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

### <span data-ttu-id="e55a6-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e55a6-127">-Confirm</span></span>
<span data-ttu-id="e55a6-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e55a6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e55a6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e55a6-129">-WhatIf</span></span>
<span data-ttu-id="e55a6-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e55a6-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e55a6-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e55a6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e55a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55a6-132">CommonParameters</span></span>
<span data-ttu-id="e55a6-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e55a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55a6-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e55a6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55a6-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e55a6-135">INPUTS</span></span>

### <span data-ttu-id="e55a6-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="e55a6-136">None</span></span>

## <span data-ttu-id="e55a6-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e55a6-137">OUTPUTS</span></span>

### <span data-ttu-id="e55a6-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e55a6-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="e55a6-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e55a6-139">NOTES</span></span>

## <span data-ttu-id="e55a6-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e55a6-140">RELATED LINKS</span></span>
